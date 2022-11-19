<script lang="ts">
    export let orderNumber: string;
    export let data: string;
    export let value: string;
    export let deliveryType: string;
    export let status: string;
</script>

<tr class="sales_table_line">
    <td>{orderNumber}</td>
    <td>{data}</td>
    <td>{value}</td>
    <td>{deliveryType}</td>
    <td>{status}</td>
    <td></td>
</tr>

<style>
    .sales_table_line {
        border-bottom: 1px solid black;
        text-align: center;
        height: 40px;
    }
</style>