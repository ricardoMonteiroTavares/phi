<script lang="ts">
	import SalesTableLine from "./SalesTableLine.svelte";

    const sales = [
        {
            orderNumber: '0001',
            data: '17/11/2022',
            value: '150,00',
            deliveryType: 'Em Casa',
            status: 'Aguardando Pgto'
        },
        {
            orderNumber: '0002',
            data: '18/11/2022',
            value: '20,00',
            deliveryType: 'Buscar Loja',
            status: 'Pago'
        },
        {
            orderNumber: '0003',
            data: '18/11/2022',
            value: '200,00',
            deliveryType: 'Buscar Loja',
            status: 'Cancelada'
        },
    ];
</script>

<table class="sales_table">
    <tr class="sales_table_header">
        <th>Nº Pedido</th>
        <th>Data</th>
        <th>Valor (R$)</th>
        <th>Tipo de Entrega</th>
        <th>Status</th>
        <th>Ações</th>
    </tr>
    {#each sales as sale}
        <SalesTableLine {...sale} />
    {/each}
</table>

<style>
    .sales_table {
        width: 100%;
        border-collapse: collapse; 
    }

    .sales_table_header {
        border-bottom: 1px solid black;
        text-align: center;
        height: 40px;
    }
</style>