<script lang="ts">
	import Icon from "../Icon.svelte";

    export let name: string;    
</script>

<button class="icon_button" on:click={() => {}}>
    <Icon {name} width='20px' />
</button>

<style>
    .icon_button {
        width: 30px;
        height: 30px;
        border-radius: 5px;        
        padding: 0px;
        border: 1px solid var(--color);
        display: flex;
        align-items: center;
        justify-content: center;
        cursor: pointer;   
        background-color: white;
        fill: var(--color);
    }
    .icon_button:hover {        
        background-color: var(--color);
        border: none;
        fill: white;
    }
</style>