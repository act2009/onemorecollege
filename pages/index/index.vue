<template>
	<view class="index">
		
		
		<IndexSwiper></IndexSwiper>
		<Icons></Icons>
		
		<Card cardTitle="推荐课程" goName="查看更多"></Card>
		<SingleCommodityList></SingleCommodityList>
		<Card cardTitle="专题" goName="查看更多"></Card>
         <ThematicList></ThematicList>
		<Card cardTitle="新上好课" goName="查看更多"></Card>
		<SingleCommodityList></SingleCommodityList>
		
		<Card cardTitle="另一个课程样式" goName="查看更多"></Card>
			<CommondityList></CommondityList>
	</view>
	
</template>

<script>
	import IndexSwiper from '@/components/index/IndexSwiper.vue'
	import Icons       from '@/components/common/Icons.vue'
	import Card        from '@/components/common/Card.vue'
	import SingleCommodityList from '@/components/common/SingleCommodityList.vue'
	import ThematicList    from '@/components/common/ThematicList.vue'
	import CommondityList  from '@/components/common/CommondityList.vue'
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
			SingleCommodityList,
			ThematicList,
			CommondityList
		
		},
		onLoad() {

		},
		methods: {

		}
	}
</script>

<style>
</style>
