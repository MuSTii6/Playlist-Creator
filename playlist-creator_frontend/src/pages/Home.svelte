<script>
</script>

<body>
    <div class="my-5" style="text-align: center">
        <img
            class="img-fluid logo"
            alt="Svelte Logo"
            src="images/img-playlist.png"
        />
    </div>

    <a href="http://localhost:8080/#/artists">
        <button>Klick hier um einen Song auszusuchen</button>
    </a>
</body>

<style>
    .logo {
        height: 400px;
        top: 29rem;
        left: 52rem;
        background-color: #000000;
        position: absolute;
    }

    button {
        font-weight: bold;
        background: #ffffff;
        color: #000000;
        border-color: #f01c64;
        border-radius: 60px;
        border-width: 3px;
        padding: 0.75rem 1.5rem;
        cursor: pointer;
        top: 52rem;
        left: 43%;
        position: absolute;
    }
    button:hover {
        background: #f01c64;
        color: #ffffff;
        border-color: #ffffff;
    }

    body {
        background: #000000;
    }
</style>
