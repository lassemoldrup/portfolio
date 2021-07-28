<script lang="ts">
    import About from './components/About.svelte';
    import ChessIcon from './icons/chess.svg';
    import LambdaIcon from './icons/lambda.svg';
</script>


<style lang="scss">
    #grid {
        width: 100%;
        display: grid;
        grid-template: 100vw 100vw 100vw / 100vw;

        @media only screen and (min-width: 667px) {
            grid-template: 50vw 50vw auto / 1fr 1fr;
        }
        @media only screen and (min-width: 1000px) {
            grid-template: 33vw auto / 1fr 1fr 1fr;
        }
    }

    .tile {
        padding: 5%;
        display: flex;
        flex-direction: column;
        overflow: hidden;
        transition: background-color 80ms cubic-bezier(0, 0, 0.5, 1);
        font-size: 1.2rem;

        p {
            margin: 0;
        }

        h2 {
            text-align: center;
            margin-bottom: calc(10% - 0.5rem);
            margin-top: 0;
            line-height: 1em;
        }

        :global(.icon) {
            width: 100%;
            max-height: 100%;
            flex-grow: 1;
            fill: var(--lighter);
            transition: max-height 150ms cubic-bezier(0, 0, 0.5, 1), opacity 150ms cubic-bezier(0, 0, 0.5, 1);
            transform: scale(0.5);
        }

        &:hover, &:focus {
            cursor: pointer;

            :global(.icon) {
                max-height: 0;
                opacity: 0;
            }

            .description {
                opacity: 100;
            }
        }
    }

    .description {
        opacity: 0;
        height: 0;
        transition: opacity 150ms cubic-bezier(0, 0, 0.5, 1);
    }

    #chess-tile {
        //background-color: hsl(268, 15%, 30%);
        background-color: hsl(203, 15%, 30%);

        &:hover, &:focus {
            //background-color: hsl(268, 15%, 15%);
            background-color: hsl(203, 15%, 15%);
        }
    }

    #lambda-tile {
        //background-color: hsl(140, 15%, 30%);
        background-color: hsl(347, 15%, 30%);

        &:hover, &:focus {
            background-color: hsl(347, 15%, 15%);
        }
    }

    #sat-tile {
        background-color: hsl(55, 15%, 30%);

        &:hover, &:focus {
            background-color: hsl(55, 15%, 15%);
        }
    }
</style>


<div id="grid">
    <div id="chess-tile" class="tile">
        <h2>Chess engine</h2>
        <ChessIcon class="icon"/>
        <div class="description">
            <p>A UCI-compatible chess engine written in Rust.</p>
            <h3>Tech</h3>
            <ul>
                <li>Rust</li>
                <li>WebAssembly</li>
            </ul>
        </div>
    </div>
    <div id="lambda-tile" class="tile">
        <h2>Lambda calculus</h2>
        <LambdaIcon class="icon"/>
        <div class="description">
            <p>A lambda calculus interpretter written in Rust.
            It supports macros along with different evaluation orders.</p>
            <h3>Tech</h3>
            <ul>
                <li>Rust</li>
                <li>WebAssembly</li>
            </ul>
        </div>
    </div>
    <div id="sat-tile" class="tile">
        <h2>Sat solver</h2>
        <ChessIcon class="icon"/>
        <div class="description">
            <p>A SAT-solver written in Rust.</p>
            <h3>Tech</h3>
            <ul>
                <li>Rust</li>
                <li>WebAssembly</li>
            </ul>
        </div>
    </div>
</div>
<About/>
