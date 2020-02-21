<template>
	<view class="commondity">
			<!--单个课程组件-->
			<view class="commondity-item"
			v-for="(item,index) in dataList" :key="index">
					<image class="commondity-img"  :src="item.imgUrl" mode=""></image>
				<view class="commondity-content">
					<text class="commondity-name">{{item.name}}</text>
					<view>
						<text class="cprice">¥{{item.cprice}}</text>
						<text class="oprice color999">¥{{item.oprice}}</text>
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
	.commondity{
		display: flex;
		flex-wrap: wrap;
		align-items: center;
	    justify-content: space-between;
	}
	.commondity-item{
		width: 45%;
		padding-bottom: 20rpx;

	}
	.commondity-img{
		width: 100%;
		height: 210rpx;
		border-radius: 8rpx;
	}
	.commondity-content{
		text-align: center;
	}
	.commondity-name{
		overflow: hidden;
		text-overflow: ellipsis;
		display: -webkit-box;
		-webkit-line-clamp:2;
		-webkit-box-orient:vertical;
		color: #333333;
		word-break: break-all;
		padding:6rpx 20rpx;
		
	}
	.cprice{
	color: #fb6161;
	}
	.oprice{
		padding-right: 10rpx;
		text-decoration: line-through;
		font-size: 24rpx;
	}
	
</style>
