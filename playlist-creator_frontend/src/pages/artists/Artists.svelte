<script>
    import axios from "axios";
    import { HtmlTag } from "svelte/internal";

    let artists = [];

    function getArtists() {
        axios.get("http://localhost:3001/api/artists").then((response) => {
            artists = response.data;
        });
    }
    getArtists();
</script>

{window.scrollTo(0, 1100)}

<div class="mb-5">
    <h1 class="mt-3">Liste hinzugefügter Songs</h1>

    <a href="#/create-artist">Song hinzufügen</a>
    <br />
    <br />
    <table
        class="table"
        style="color: #f01c64; background-color:white; border-color: #f01c64; border-radius: 20px"
    >
        <thead>
            <tr>
                <th>ID</th>
                <th>Titel</th>
                <th>Künstler</th>
            </tr>
        </thead>
        <tbody>
            {#each artists as artist}
                <tr>
                    <td>
                        <a href={"#/artists/" + artist._id}>
                            {artist._id}
                        </a>
                    </td>
                    <td>
                        {artist.name}
                    </td>
                    <td>
                        {artist.origin}
                    </td>
                </tr>
            {/each}
        </tbody>
    </table>
</div>

<a href="http://localhost:8080/#/albums">
    <button>Hier gehts weiter zu den Playlists</button>
</a>

<style>
    button {
        font-weight: bold;
        background: #ffffff;
        color: #000000;
        border-color: #f01c64;
        border-radius: 60px;
        border-width: 3px;
        padding: 0.75rem 1.5rem;
        cursor: pointer;
        top: 135rem;
        margin-left: 25rem;
    }
    button:hover {
        background: #f01c64;
        color: #ffffff;
        border-color: #ffffff;
    }
</style>
