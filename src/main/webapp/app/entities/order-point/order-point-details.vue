<template>
    <div class="row justify-content-center">
        <div class="col-8">
            <div v-if="orderPoint">
                <h2 class="jh-entity-heading"><span>OrderPoint</span> {{orderPoint.id}}</h2>
                <dl class="row jh-entity-details">
                    <dt>
                        <span>Number</span>
                    </dt>
                    <dd>
                        <span>{{orderPoint.number}}</span>
                    </dd>
                    <dt>
                        <span>Goods</span>
                    </dt>
                    <dd>
                        <div v-if="orderPoint.goods">
                            <router-link :to="{name: 'GoodsView', params: {goodsId: orderPoint.goods.id}}">{{orderPoint.goods.name}}</router-link>
                        </div>
                    </dd>
                    <dt>
                        <span>Orders</span>
                    </dt>
                    <dd>
                        <div v-if="orderPoint.orders">
                            <router-link :to="{name: 'OrdersView', params: {ordersId: orderPoint.orders.id}}">{{orderPoint.orders.id}}</router-link>
                        </div>
                    </dd>
                </dl>
                <button type="submit"
                        v-on:click.prevent="previousState()"
                        class="btn btn-info">
                    <font-awesome-icon icon="arrow-left"></font-awesome-icon>&nbsp;<span> Back</span>
                </button>
                <router-link v-if="orderPoint.id" :to="{name: 'OrderPointEdit', params: {orderPointId: orderPoint.id}}" tag="button" class="btn btn-primary">
                    <font-awesome-icon icon="pencil-alt"></font-awesome-icon>&nbsp;<span> Edit</span>
                </router-link>
            </div>
        </div>
    </div>
</template>

<script lang="ts" src="./order-point-details.component.ts">
</script>
