<script lang="ts">
    export let header: string;
    export let description: string;
    export let color: string;
    export let hoverColor: string;
    export let techs: string[];
</script>


<style lang="scss">
    .tile {
        padding: 5%;
        display: flex;
        flex-direction: column;
        overflow: hidden;
        transition: background-color 80ms cubic-bezier(0, 0, 0.5, 1);
        font-size: 1.2rem;
        background-color: var(--bg-color);

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

        :global(.icon .stroke) {
            stroke: var(--lighter);
        }

        &:hover, &:focus {
            background-color: var(--hover-color);
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
</style>


<div class="tile" style="--bg-color: {color}; --hover-color: {hoverColor}">
    <h2>{header}</h2>
    <slot/>
    <div class="description">
        <p>{description}</p>
        <h3>Tech</h3>
        <ul>
            {#each techs as tech}
            <li>{tech}</li>
            {/each}
        </ul>
    </div>
</div>