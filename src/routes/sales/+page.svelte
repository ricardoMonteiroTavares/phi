<script>
	import Card from "$lib/component/Card/Card.svelte";

	import SalesTable from "$lib/component/table/SalesTable/SalesTable.svelte";

</script>
<svelte:head>
	<title>Vendas</title>
	<meta name="description" content="Ver todas as vendas no sistema" />
</svelte:head>

<section>
    <h1>Vendas</h1>
    <Card>
        <SalesTable />
    </Card>
</section>