<script lang="ts">
	import DeliveryBadge from "$lib/component/badges/DeliveryBadge.svelte";
	import StatusBadge from "$lib/component/badges/StatusBadge.svelte";

	import type { DeliveryEnum } from "$lib/core/enum/DeliveryEnum";
    import type { StatusEnum } from "$lib/core/enum/StatusEnum";

    export let orderNumber: string;
    export let data: string;
    export let value: string;
    export let deliveryType: string;
    export let status: string;
    export let lastLine: boolean;

    const _status: StatusEnum = <StatusEnum> status;
    const _delivery: DeliveryEnum = <DeliveryEnum> deliveryType;
</script>

<tr class="sales_table_line {lastLine ? 'sales_table_last_line' : ''}">
    <td>{orderNumber}</td>
    <td>{data}</td>
    <td>{value}</td>
    <td><DeliveryBadge delivery={_delivery} /></td>
    <td><StatusBadge status={_status} /></td>
    <td></td>
</tr>

<style>
    .sales_table_line {
        border-bottom: 1px solid var(--primary-color-dark);        
        height: 40px;
    }
    
    .sales_table_last_line {
        border-bottom: 0px;
    }
    
    .sales_table_line td {
        text-align: -webkit-center;
        text-align: -moz-center;
    }
</style>