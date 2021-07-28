<script lang="ts">
    import GithubIcon from '../icons/github.svg';
    import HomeIcon from '../icons/home.svg';
</script>


<style lang="scss">
    $header-height: 50px;

    header {
        width: 100%;
        height: $header-height + 1px;
        background-color: #333;
        border-bottom: 1px solid #555;

        :global(.icon) {
            fill: var(--lighter);
            width: auto;
            height: 100%;
        }
    }

    nav {
        display: inline-block;

        li {
            border-right: 1px solid #555;
        }
    }

    ul {
        margin: 0;
        padding: 0;
        list-style-type: none;
        height: 100%;
        display: inline-flex;
    }

    li {
        display: inline-block;
    }

    #links {
        float: right;

        .icon-link {
            border-left: 1px solid #555;
        }
    }

    .icon-link, .text-link {
        height: $header-height;
        text-align: center;
        padding: 10px;

        &:hover, &:focus {
            background-color: #222;
            cursor: pointer;
        }
    }

    .icon-link {
        width: $header-height + 1px;

        &:hover, &:focus {
            :global(.icon) {
                fill: var(--light);
            }
        }
    }

    .text-link {
        font-size: 25px;

        a {
            color: var(--lighter);
            text-decoration: none;
        }
    }
</style>


<header>
    <nav>
        <ul>
            <li class="icon-link">
                <a href="/"><HomeIcon class="icon"/></a>
            </li>
            <li class="text-link">
                <a href="#about">ABOUT</a>
            </li>
        </ul>
    </nav>
    <ul id="links">
        <li class="icon-link">
            <a href="https://github.com/lassemoldrup"><GithubIcon class="icon"/></a>
        </li>
    </ul>
</header>