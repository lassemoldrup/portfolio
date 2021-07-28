<script lang="ts">
    import Header from './components/Header.svelte';
    import Home from './Home.svelte';
    import '../node_modules/normalize.css/normalize.css';
</script>


<style lang="scss" global>
    :root {
        --lighter: #EEE;
        --light: #BBB;
    }

    *, *::before, *::after {
        box-sizing: border-box;
    }

    html {
        font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
        color: var(--lighter);
    }

    body {
        background: #222;
    }

    h1, h2, h3 {
        text-transform: uppercase;
        font-weight: normal;
        letter-spacing: 2px;
    }

    a {
        text-decoration: none;
        color: lightblue;

        &:hover, &:focus {
            text-decoration: underline;
        }
    }

    p {
        line-height: 1.5em;
    }
</style>


<Header/>
<Home/>
