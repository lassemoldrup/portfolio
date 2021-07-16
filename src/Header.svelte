<script lang="ts">
    import GithubIcon from './icons/github.svg';
    import HomeIcon from './icons/home.svg';
</script>


<style lang="scss">
    $header-height: 50px;

    header {
        width: 100%;
        height: $header-height;
        background-color: #333;
    }

    nav {
        display: inline-block;
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
    }

    .icon-link, .text-link {
        height: $header-height;
        text-align: center;
        padding: 6px;
        border: 2px solid #333;

        &:hover, &:focus {
            border: 2px solid var(--light);
            cursor: pointer;
        }
    }

    .icon-link {
        width: $header-height;

        &:hover, &:focus {
            :global svg {
                fill: var(--light);
            }
        }
    }

    :global svg {
        fill: var(--lighter);
        width: auto;
        height: 100%;
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
                <a href="#"><HomeIcon/></a>
            </li>
            <li class="text-link">
                <a href="#">ABOUT</a>
            </li>
        </ul>
    </nav>
    <ul id="links">
        <li class="icon-link">
            <a href="https://github.com/lassemoldrup"><GithubIcon/></a>
        </li>
    </ul>
</header>