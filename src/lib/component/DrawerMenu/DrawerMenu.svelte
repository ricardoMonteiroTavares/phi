<script>
	import DrawerMenuItem from "./DrawerMenuItem.svelte";

    const items = [
        {name: "Dashboard", path: "/"},
        {name: "Vendas", path: "/sales"},
        {name: "Produtos", path: "/items"},
    ]

</script>
<div class="drawer_menu">
    {#each items as item}
        <DrawerMenuItem {...item} />
    {/each}
     
</div>

<style>
    .drawer_menu {
        height: 100vh;
        width: 210px;
        background-color: var(--primary-color);
        padding-left: 15px;
        padding-right: 15px;
    }    
</style>