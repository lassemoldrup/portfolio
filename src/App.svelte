<script lang="ts">
    import Home from './Home.svelte';
    import '../node_modules/normalize.css/normalize.css';
</script>


<style lang="scss" global>
    :root {
        --lighter: #EEE;
        --light: #BBB;
    }

    * {
        box-sizing: border-box;
    }

    html {
        font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
        color: var(--lighter);
    }

    body {
        background: #222;
    }

    a {
        text-decoration: none;
        color: lightblue;

        &:hover, &:focus {
            text-decoration: underline;
        }
    }
</style>


<Home/>
