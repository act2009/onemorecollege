<template>
	<view class="index">
		
		
		<IndexSwiper></IndexSwiper>
		<Icons></Icons>
		
		<Card cardTitle="推荐课程"></Card>
		<SingleCommodityList></SingleCommodityList>
		<Card cardTitle="a"></Card>
		
	</view>
	
</template>

<script>
	import IndexSwiper from '@/components/index/IndexSwiper.vue'
	import Icons       from '@/components/common/Icons.vue'
	import Card        from '@/components/common/Card.vue'
	import SingleCommodityList from '@/components/common/SingleCommodityList.vue'
	
	export default {
		data() {
			return {
				title: 'Hello'
			}
		},
		components:{
			IndexSwiper,
			Icons,
			Card,
			SingleCommodityList
		
		},
		onLoad() {

		},
		methods: {

		}
	}
</script>

<style>
</style>
