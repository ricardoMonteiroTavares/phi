<script>
	import DrawerMenuItem from "./DrawerMenuItem.svelte";

</script>
<div class="drawer_menu">
    <DrawerMenuItem name="Dashboard"/>
    <DrawerMenuItem name="Vendas"/>
    <DrawerMenuItem name="Produtos"/>    
</div>

<style>
    .drawer_menu {
        height: 100%;
        width: 210px;
        background-color: blueviolet;
        padding-left: 15px;
        padding-right: 15px;
    }    
</style>