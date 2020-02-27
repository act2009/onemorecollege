<template>
			<!-- 评论 -->
	<view class="comments">
	
	<view class="comments-item"
	v-for="(item,index) in dataList"
	:key="index"
	>
		<view class="commentsitem-name">
			<image class="comments-avatar" :src="item.avatar" mode="scaleToFill"></image>
			<text class="uname colorgrey">{{item.uname}}</text>
		</view>
		<view class="commentsitem-content">
			{{item.content}}
		</view>
		<view class="commentsitem-time">
			<text class="reply-time color999">{{item.create_time}}</text>
		</view>
		<view class="commentsitem-reply">
			<text class="colorgreen">[课程团队回复]</text>
			<text class="reply-team colorgrey">听得懂，用得上，这也是我们理想中课程的样子！谢谢你的学习感受，给了老师和课程团队极大动力，努力用心做好内容！</text>
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
	.comments-item{
		display: flex;
		flex-direction:column;
		flex-wrap: wrap;
		padding: 20rpx 0;
		border-bottom: 1rpx solid #F2F4F7;
	}
	.commentsitem-name{
		display: flex;
		flex-wrap: nowrap;
		align-items: center;
		padding: 20rpx 0;
	}
	.comments-avatar{
		width:80rpx;
		height: 80rpx;
		border-radius: 50%;
		vertical-align: middle;
		justify-content: center;
	}
	.uname{
		margin-left: 32rpx;
	}
	.commentsitem-content{
		
	}
	.commentsitem-time{
		width: 100%;
		display: flex;
		flex-direction: row;
	}
	.reply-time{
		margin-left: auto;
		margin-right: 0;
		padding: 10rpx 0;
	}
	.commentsitem-reply{
		display: flex;
		flex-wrap: wrap;
		padding: 30rpx 16rpx;
/* 		background-color: #f2f4f7; */
/* 		border-radius: 6rpx; */
	}
	
</style>
