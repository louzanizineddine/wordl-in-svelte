<script>

import {board} from "../store";
import Cell from "./Cell.svelte";
</script>

<div class="game">
    {#each $board as column , y}
        <div class="row">
            {#each column as row , x}
                <Cell {y} , {x}/>

            {/each}
        </div>
    {/each}
</div>

<style>
    .game {
        margin: 15px auto;
        width: fit-content

    }
    .row {
        display: flex;
    }
</style>