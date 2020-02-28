<template>
	<!--标题名称-导航名称-->
	<view class="card">
		<view class="card-name"
		 :style="'font-size:'+fontSize+';'
		 +'font-weight:'+fontWeight+';'
		 +'padding:'+paddingData+';'"
		 >
		 {{cardTitle}}</view>
		<view class="card-nav" 
		 :style="'padding:'+paddingData+';'" to="/course/">{{goName}}</view>
	</view>
</template>

<script>
	export default{
		props:{
			cardTitle:{
				type:String,
				default:""
			},
			goName:{
				type:String,
				default:""
			},
			fontSize:{
				type:String,
				default:"32rpx"
			},
			fontWeight:{
				type:String,
				default:"bold"
			},
			paddingData:{
				type:String,
				default:"30rpx 0"
			}
		}
	}
</script>

<style scoped>
	.card{
		width: 100%;
		display: flex;
		flex-direction: row;
		align-items: center;
		
	}
	.card-name{
        width: 80%;
	}
	.card-nav{
		align-self: baseline;
        margin-left: auto;
		margin-right: 0;
		font-size: 28rpx;
		color: #999999;


	}
</style>
