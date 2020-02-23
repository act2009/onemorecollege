<template>
	<!--单个广告组件-->
	<view class="thematic">
		<view class="thematic-item"
		v-for="(item,index) in dataList" :key="index">
			<image class="thematicitem-img" :href="item.url" :src="item.imgUrl" mode=""></image>
		</view>
	</view>
</template>

<script>
	export default{
		props:{
			dataList:Array
		}
	}
	
</script>

<style scoped>
	.thematic{
/* 		display: flex;
		flex-wrap: wrap;
		align-items: center; */


	}
	.thematic-item{
		
	}
	.thematicitem-img{
		width: 100%;
		height: 350rpx;
		padding-bottom: 10rpx;
	}
	
</style>
