<template>
	<view class="video-list">
		<!--video-->
		<swiper @change="onChangeTab"  :current="selectedIndex" 
		:style="'height:'+clientHight+'px;'"
		:duration="0"
		>
			<swiper-item v-for="(item,index) in videolist" :key="index" 
			@touchmove.stop="catchTouchMove"
			>
				<view class="home-data">
					<Video :videoSrc="item.videoSrc"></Video>
				</view>
			</swiper-item>
		</swiper>
		<!--video-->
		<view class="video-intro">
			<Card 	cardTitle="来自福布斯精英的25节课来自福布斯精英的25节课" goName="详情"></Card>
			<text class="color999">共50课时</text>
		     <view class="intro-bottom"></view>
		</view>
		
		<scroll-view class="scroll-content" scroll-x="true"
		:scroll-into-view="scrollIntoIndex"
		 >

	<view class="scroll-items "
	:id="'vi'+index"
	v-for="(item,index) in videolist"
	:key="index"
	@tap="changeTab(index)"
	
	>
	<view :class="selectedIndex===index? 'items-content-active':'items-content'">
		<view :class=" selectedIndex===index? 'items-active-background':'items-background'">视频</view>
		<text class="i-content" :style=" selectedIndex===index?'color:#339966':'color:#333'">{{item.name}}</text>
	</view>

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
				//选中的索引
				selectedIndex:0,
				//videlist滑动跟随的索引
				scrollIntoIndex:"vi0",
				//数据高度
				clientHight:0,
				videolist:[
					{
						id:1,
						name:"第1课",
						videoSrc:"http://recordcdn.quklive.com/upload/vod/user1452045053897990/1582179681187957/4/video.mp4",
					},
					{
						id:2,
						name:"第2课",
						videoSrc:"http://recordcdn.quklive.com/upload/vod/user1452045053897990/1582275911518954/4/video.mp4",
					},
					{
						id:3,
						name:"第3课",
						videoSrc:"http://recordcdn.quklive.com/upload/vod/user1452045053897990/1581491296898984/8/video.m3u8",
					},
					
				]
				
			}
		},
		components:{
			Video,
			Card
		},
		onLoad() {
			
		},
		onReady() {
			let view=uni.createSelectorQuery().select('.home-data');
						view.boundingClientRect(data => {
							this.clientHight=data.height;
			 console.log(data.height);
						}).exec();
		},
		methods:{
			changeTab(index){
				if(this.selectedIndex===index){
					return;
				}
				this.selectedIndex=index;
				this.scrollIntoIndex='vi'+index;
			},
			onChangeTab(e){
				this.changeTab(e.detail.current);
			},
			//禁止用户滑动视频列表
			catchTouchMove(){
				return false;
			}
		}
	}
</script>

<style scoped>
	uni-view{
		line-height: 1.4;
	}
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
/* 		border-radius: 4rpx; */
/* 		border: 1rpx solid #C0C0C0; */
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
		overflow: hidden;
		text-overflow: ellipsis;
		display: -webkit-box;
		-webkit-line-clamp:2;
		-webkit-box-orient:vertical;
		word-break: break-all;
		padding:6rpx 20rpx;
	}
</style>
