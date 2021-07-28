<script lang="ts">
    import About from './components/About.svelte';
    import Tile from './components/Tile.svelte';
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
</style>


<div id="grid">
    <Tile header="Chess engine"
        description="A UCI-compatible chess engine written in Rust."
        color="hsl(203, 15%, 30%)"
        hoverColor="hsl(203, 15%, 15%)"
        techs="{['Rust', 'WebAssembly']}">
        <ChessIcon class="icon"/>
    </Tile>

    <Tile header="Lambda calculus"
        description="A lambda calculus interpretter written in Rust.
            It supports macros along with different evaluation orders."
        color="hsl(347, 15%, 30%)"
        hoverColor="hsl(347, 15%, 15%)"
        techs="{['Rust', 'WebAssembly']}">
        <LambdaIcon class="icon"/>
    </Tile>

    <Tile header="Sat solver"
        description="A SAT solver written in Rust."
        color="hsl(55, 15%, 30%)"
        hoverColor="hsl(55, 15%, 15%)"
        techs="{['Rust', 'WebAssembly']}">
        <LambdaIcon class="icon"/>
    </Tile>
</div>
<About/>
