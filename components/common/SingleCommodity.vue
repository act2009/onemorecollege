<template>

	<view class="singleCommodity">
			<!--横向单个商品组件，公用-->
		<view class="singleCommodity-item"
		v-for="(item,index) in dataList" :key="index">
		<view class="singleCommodity-left">
			<image class="singleCommodity-img" :src="item.imgUrl" mode=""></image>
		</view>
		
		<view class="singleCommodity-right">
			<view class="right-title">{{item.name}}</view>
			<view class="right-desc color999">{{item.description}}</view>
			<view class="right-bottom">
				<text class="bottom-left color999">{{item.purchased}}人开通</text>
				<text class="bottom-right">
					
					<text class="oprice color999">¥{{item.oprice}}</text>
					<text class="cprice">¥{{item.cprice}}</text>

					</text>
			</view>
		</view>
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
	.singleCommodity{


	}
	.singleCommodity-item{
		display: flex;
		flex-direction: row;
		padding-bottom: 40rpx;
	}
	.singleCommodity-left{
			height: 210rpx;
	}
	.singleCommodity-img{
		width: 280rpx;
		height: 210rpx;
		border-radius: 8rpx;
	}
	
	.singleCommodity-right{
		padding: 4rpx 0 4rpx 20rpx;
		height: 210rpx;
		display: flex;
		flex-wrap: wrap;
		align-items: center;
	}
	.right-title{
		width: 100%;
		line-height: 1.4;
		font-size: 30rpx;
		font-weight: bold;
		overflow: hidden;
		text-overflow: ellipsis;
		display: -webkit-box;
		-webkit-line-clamp:1;
		-webkit-box-orient:vertical;
		word-break: break-all;
	}
	.right-desc{
		width: 100%;
		font-size: 28rpx;
		line-height: 1.4;
		overflow: hidden;
		text-overflow: ellipsis;
		display: -webkit-box;
		-webkit-line-clamp:2;
		-webkit-box-orient:vertical;
		word-break: break-all;
	}
	.right-bottom{
		width: 100%;
		display: flex;
		
	}
	.bottom-left{
	
	}
	.bottom-right{
		flex-direction:row-reverse;
		color: #fb6161;
		margin-left: auto;
		margin-right: 0;
	}
	
	.oprice{
		padding-right: 10rpx;
		text-decoration: line-through;
		font-size: 24rpx;
	}
	

	
	
</style>
