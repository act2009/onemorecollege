<template>
	<view class="video-list">
		<Video :dataList="videolist"></Video>
		<view class="video-intro">
			<Card 	cardTitle="来自福布斯精英的25节课来自福布斯精英的25节课" goName="详情"></Card>
			<text class="color999">共50课时</text>
		     <view class="intro-bottom"></view>
		</view>
		
		<scroll-view class="scroll-content" scroll-x="true" >

	<view class="scroll-items">
		<view class="item-icon">视频</view>
		<text class="i-content">来自福布斯精英的25节课25节课</text>
	</view>
	<view class="scroll-items">
		<view class="item-icon">视频</view>
		<text class="i-content">来自福布斯精英的25节课25节课</text>
	</view>
	<view class="scroll-items">
		<view class="item-icon">视频</view>
		<text class="i-content">来自福布斯精英的25节课25节课</text>
	</view>

		</scroll-view>
	</view>
</template>

<script>
	import Video from '@/components/course/Video.vue'
	import Card  from '@/components/common/Card.vue'
	export default{
		data(){
			return{
				videolist:[
					{
						id:1,
						name:"第1课",
						videoSrc:"http://recordcdn.quklive.com/upload/vod/user1452045053897990/1582179681187957/4/video.mp4",
					}
				]
				
			}
		},
		components:{
			Video,
			Card
		}
	}
</script>

<style scoped>
	.video-intro{
		display: flex;
		flex-wrap: wrap;
	}
	.intro-bottom{
		width: 100%;
		height: 20rpx;
		border-bottom: 1rpx solid #F2F4F7;
	}
	.scroll-content{
		width: 100%;
		height: 240rpx;
		white-space: nowrap;
	}
	.scroll-items{
		width: 340rpx;
		height: 200rpx;
		margin: 0 20rpx;
		border-radius: 4rpx;
		border: 1rpx solid #09BB07;
		display: inline-block;
		
	}
	.item-icon{
		width: 40rpx;
        background-color:#09BB07;
		margin: 10rpx 0;
	  	padding: 2rpx 10rpx;
	  	font-size: 20rpx;
	  	color:#FFFFFF;
	  
	}
	.i-content{
		white-space:normal;
		align-self: center;
	}
</style>
