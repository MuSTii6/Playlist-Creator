<script>
    import axios from "axios";

    export let params = {};

    let id;

    $: {
        // "Reactive Statement":
        // This block of is executed whenever the value of a variable in it changes.
        // See https://svelte.dev/tutorial/reactive-statements
        id = params.id;
        getArtist();
    }

    let artist = {};

    function getArtist() {
        axios.get("http://localhost:3001/api/artists/" + id)
            .then((response) => {
                artist = response.data;
            });
    }
</script>

<div class="mb-5">
    <h1 class="mt-3">Song (ID: {id})</h1>
    <p>Titel: {artist.name}</p>
    <p>Künstler: {artist.origin}</p>
</div>
