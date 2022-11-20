<script lang="ts">
	import { StatusEnum } from "$lib/core/enum/StatusEnum";

    export let status: StatusEnum;

    function getColor(s:StatusEnum) {
        switch (s) {
            case StatusEnum.AG_PGTO:
                return 'background-color: #fcb41d; color: black';
            case StatusEnum.AG_LIB:
                return 'background-color: #f77f00; color: black';
            case StatusEnum.LIB_ENTREGA:
                return 'background-color: #4cc9f0; color: black';
            case StatusEnum.ENTRGANDO:
                return 'background-color: #3794fc; color: white';
            case StatusEnum.FINALIZADA:
                return 'background-color: #51c81c; color: white';
            case StatusEnum.CANCELADA:
                return 'background-color: #fc381d; color: white';
        }
    }
</script>

<div class="status_badge" style="{getColor(status)}">
    <h6>{status.valueOf()}</h6>
</div>

<style>
    .status_badge {
        width: 135px;
        height: 20px;
        border-radius: 20px;
        text-align: center;
    }
    .status_badge h6 {
        display: inline;        
    }
</style>