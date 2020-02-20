<template>
	<view class="index">
		
		
		<IndexSwiper></IndexSwiper>
		<Icons></Icons>
		
		<Card></Card>
		
	</view>
	
</template>

<script>
	import IndexSwiper from '@/components/index/IndexSwiper.vue'
	import Icons       from '@/components/common/Icons.vue'
	import Card        from '@/components/common/Card.vue'
	
	
	export default {
		data() {
			return {
				title: 'Hello'
			}
		},
		components:{
			IndexSwiper,
			Icons,
			Card
		
		},
		onLoad() {

		},
		methods: {

		}
	}
</script>

<style>
</style>
