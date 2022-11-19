<script lang="ts">
    import { page } from '$app/stores';
    export let name: string;
    export let path: string;    
</script>

<a 
    class="drawer_menu_item" 
    aria-current={$page.url.pathname === path ? 'page' : undefined}
    href={path}
>
    {name}
</a>

<style>
    .drawer_menu_item {
        display: flex;
        align-items: center;
        height: 40px;
        width: 100%;
        color: var(--background-color);   
        padding-left: 5px;  
        margin-top: 5px;
        margin-bottom: 5px;
        text-decoration: none;
    }

    .drawer_menu_item[aria-current='page'], .drawer_menu_item:hover {
        background-color: var(--background-color);
        color: var(--primary-color);
        border-radius: 5px;
        transition-duration: 0.45s;
    }
</style>