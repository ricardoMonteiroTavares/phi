<script lang="ts">
	import { DeliveryEnum } from "$lib/core/enum/DeliveryEnum";

    export let delivery: DeliveryEnum;

    function getColor(d:DeliveryEnum) {
        switch (d) {
            case DeliveryEnum.HOME:
                return 'background-color: #fcb41d; color: black';
            case DeliveryEnum.STORE:
                return 'background-color: #3794fc; color: white';
        }
    }
</script>

<div class="delivery_badge" style="{getColor(delivery)}">
    <h6>{delivery.valueOf()}</h6>
</div>

<style>
    .delivery_badge {
        width: 110px;
        height: 20px;
        border-radius: 20px;
        text-align: center;
    }
    .delivery_badge h6 {
        display: inline;        
    }
</style>