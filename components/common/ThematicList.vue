<template>
	<!--广告组件列表-->
	<view class="thematicList">
		<Thematic :dataList="thematicList"></Thematic>
	</view>
</template>

<script>
	import Thematic from './Thematic.vue'
	export default{
		data(){
			return {
				thematicList:[
					{
						id:1,
						imgUrl:"../../static/img/shop.jpg",
						url:"",
						description:"专题"
						
					},
					{
						id:2,
						imgUrl:"../../static/img/shop.jpg",
						url:"",
						description:"专题"
						
					},
					{
						id:3,
						imgUrl:"../../static/img/shop.jpg",
						url:"",
						description:"专题"
						
					},
				]
				
			}
		},
		components:{
			Thematic
		}
		
	}
</script>

<style>
</style>
