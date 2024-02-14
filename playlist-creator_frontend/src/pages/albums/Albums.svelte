<script>
    import axios from "axios";

    let albums = [];

    function getAlbums() {
        axios.get("http://localhost:3001/api/albums").then((response) => {
            albums = response.data;
        });
    }
    getAlbums();
</script>

{window.scrollTo(0, 2000)}

<div class="mb-5">
    <h1 class="mt-3">Erstellte Playlists</h1>
    <table
        class="table"
        style="color: #f01c64; background-color:white; border-color: #f01c64; border-radius: 20px"
    >
        <thead>
            <tr>
                <th>ID</th>
                <th>Titel</th>
                <th>Released</th>
                <th>Playlist</th>
            </tr>
        </thead>
        <tbody>
            {#each albums as album}
                <tr>
                    <td>
                        <a href={"#/albums/" + album._id}>
                            {album._id}
                        </a>
                    </td>
                    <td>
                        {album.title}
                    </td>
                    <td>
                        {album.released}
                    </td>
                    <td>
                        {album.label}
                    </td>
                </tr>
            {/each}
        </tbody>
    </table>
</div>

<br />
<br />
<br />

<h1>Spotify Playlists</h1>
<br />
<br />

<p>
    <button
        class="btn btn-primary"
        type="button"
        data-bs-toggle="collapse"
        data-bs-target="#collapseWidthExample"
        aria-expanded="false"
        aria-controls="collapseWidthExample"
        style="text-align: center; width: 150px;"
    >
        Summer Vibes
    </button>
</p>
<div style="min-height: 120px;">
    <div class="collapse collapse-vertical" id="collapseWidthExample">
        <div
            class="card card-body"
            style="width: 1300px; background-color: black;"
        >
            <iframe
                style="border-radius:12px"
                src="https://open.spotify.com/embed/playlist/4brf6GfYHotPChGbBUEc0m?utm_source=generator&theme=1"
                width="87%"
                height="500"
                frameBorder="0"
                allowfullscreen=""
                allow="autoplay; clipboard-write; encrypted-media; fullscreen; picture-in-picture"
            />
        </div>
    </div>
</div>

<br />
<br />
<br />

<button
    class="btn btn-secondary"
    type="button"
    data-bs-toggle="collapse"
    data-bs-target="#collapseWidthExample2"
    aria-expanded="false"
    aria-controls="collapseWidthExample2"
    style="text-align: center; width: 150px;"
>
    Fitness
</button>

<div style="min-height: 120px;">
    <div class="collapse collapse-vertical" id="collapseWidthExample2">
        <div
            class="card card-body"
            style="width: 1300px; background-color: black;"
        >
            <iframe
                style="border-radius:12px"
                src="https://open.spotify.com/embed/playlist/3AisYU07VOwCQJAVq5d8vw?utm_source=generator"
                width="87%"
                height="500"
                frameBorder="0"
                allowfullscreen=""
                allow="autoplay; clipboard-write; encrypted-media; fullscreen; picture-in-picture"
            />
        </div>
    </div>
</div>

<br />
<br />
<br />

<button
    class="btn btn-third"
    type="button"
    data-bs-toggle="collapse"
    data-bs-target="#collapseWidthExample3"
    aria-expanded="false"
    aria-controls="collapseWidthExample3"
    style="text-align: center; width: 150px; "
>
    Party
</button>

<div style="min-height: 120px;">
    <div class="collapse collapse-vertical" id="collapseWidthExample3">
        <div
            class="card card-body"
            style="width: 1300px; background-color: black;"
        >
            <iframe
                style="border-radius:12px"
                src="https://open.spotify.com/embed/playlist/0NQF9ztiaVKw3NsceoWdiE?utm_source=generator"
                width="87%"
                height="500"
                frameBorder="0"
                allowfullscreen=""
                allow="autoplay; clipboard-write; encrypted-media; fullscreen; picture-in-picture"
            />
        </div>
    </div>
</div>

<br />
<br />
<br />

<button
    class="btn btn-fourth"
    type="button"
    data-bs-toggle="collapse"
    data-bs-target="#collapseWidthExample4"
    aria-expanded="false"
    aria-controls="collapseWidthExample3"
    style="text-align: center; width: 150px; "
>
    Oldschool
</button>

<div style="min-height: 120px;">
    <div class="collapse collapse-vertical" id="collapseWidthExample4">
        <div
            class="card card-body"
            style="width: 1300px; background-color: black;"
        >
            <iframe
                style="border-radius:12px"
                src="https://open.spotify.com/embed/playlist/3HmHQZ6uLFgCrvNl7jAyWD?utm_source=generator"
                width="87%"
                height="500"
                frameBorder="0"
                allowfullscreen=""
                allow="autoplay; clipboard-write; encrypted-media; fullscreen; picture-in-picture"
            />
        </div>
    </div>
</div>

<style>
    .btn {
        font-weight: bold;
        background: #e2e8f0;
        color: #000000;
        border-color: #f01c64;
        border-radius: 60px;
        border-width: 3px;
    }

    .btn:hover {
        background: #f01c64;
        color: #ffffff;
        border-color: #ffffff;
    }

    .mb-5 {
        margin-top: 50rem;
    }
</style>
