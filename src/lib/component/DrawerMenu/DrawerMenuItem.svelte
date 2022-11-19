<script lang="ts">
    import { page } from '$app/stores';
    export let name: string;
    export let path: string;    
</script>

<div 
    class="drawer_menu_item" 
    aria-current={$page.url.pathname === path ? 'page' : undefined}
>{name}</div>

<style>
    .drawer_menu_item {
        display: flex;
        align-items: center;
        height: 40px;
        width: 100%;
        color: white;     
    }

    .drawer_menu_item[aria-current='page'] {
        background-color: chocolate;
    }
</style>