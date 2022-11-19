<script lang="ts">
    export let name: string;
</script>

<div class="drawer_menu_item">{name}</div>

<style>
    .drawer_menu_item {
        display: flex;
        align-items: center;
        height: 40px;
        width: 100vh;
        color: white;     
    }
</style>