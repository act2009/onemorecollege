<template>
	<!--标题名称-导航名称-->
	<view class="card">
		<view class="card-name">{{cardTitle}}</view>
		<view class="card-nav">查看更多</view>
	</view>
</template>

<script>
	export default{
		props:{
			cardTitle:String
		}
	}
</script>

<style scoped>
	.card{
		display: flex;
		padding: 20rpx 0;
		flex-direction: row;
		align-items: center;
		
	}
	.card-name{
		padding:20rpx 0;
		font-size: 32rpx;
		font-weight: bold;


	}
	.card-nav{
        margin-left: auto;
		margin-right: 0;
		padding:20rpx 0;
		font-size: 28rpx;
		color: #999999;


	}
</style>
