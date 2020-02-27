<template>
<!-- 	课程下视频目录 -->
<view class="courseItem">

	<view class="courseItem-item"
	v-for="(item,index) in dataList"
	:key="index"
	
	>
			<text class="item-type">视频</text>
			<text class="item-name">{{item.name}}</text>
			<text class="item-trailer">{{item.visible}}</text>
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
	.courseItem{
		display: flex;
		flex-wrap: wrap;
	}
	.courseItem-item{
		width: 100%;
		display: flex;
		flex-direction: row;
		align-items:baseline;
		justify-content: space-between;
		border-bottom: 2rpx solid #F1F1F1;
		padding: 36rpx 0;

	}
	.item-type{
		border-radius: 4rpx;
		border: 1px solid #888888;
		padding: 2rpx 10rpx;
		font-size: 20rpx;
		color:#888888;
	}
	.item-name{
		text-align: left;
		width: 75%;
		font-size: 32rpx;
	}
	.item-trailer{
		font-size: 20rpx;
		color: #4CD964;
		align-self: center;
	}
</style>
