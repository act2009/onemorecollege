<template>
	<!--头部课程图片与标题-->
	<view class="header">
		
	<view class="header-content"
	v-for="(item,index) in dataList" 
	:key="index">
		<view class="header-img"><image class="header-img" :src="item.imgUrl" mode=""></image></view>
		<text class="header-title">{{item.name}}</text>
		<text class="header-description color999">{{item.description}}</text>
		
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
	.header-content{
		display: flex;
		flex-wrap: wrap;
	}
	.header-img{
		width: 100%;
		height: 560rpx;
	}
	.header-title{
		padding: 20rpx 0;
		width: 100%;
		line-height: 1.4;
		font-size: 36rpx;
	}
	.header-description{
		width: 100%;
		font-size: 32rpx;
		line-height: 1.4;
	}
</style>
