<script lang="ts">
    export let orderNumber: string;
    export let data: string;
    export let value: string;
    export let deliveryType: string;
    export let status: string;
    export let lastLine: boolean;
</script>

<tr class="sales_table_line {lastLine ? 'sales_table_last_line' : ''}">
    <td>{orderNumber}</td>
    <td>{data}</td>
    <td>{value}</td>
    <td>{deliveryType}</td>
    <td>{status}</td>
    <td></td>
</tr>

<style>
    .sales_table_line {
        border-bottom: 1px solid var(--primary-color-dark);
        text-align: center;
        height: 40px;
    }

    .sales_table_last_line {
        border-bottom: 0px;
    }
</style>