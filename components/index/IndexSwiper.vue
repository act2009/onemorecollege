<template>
	<swiper :indicator-dots="true" :circular="true" :autoplay="true" :interval="3000" :duration="1000">
		<swiper-item>
			<view class="swiper-item"><image class="swiper-img" src="../../static/img/banner1.jpg" mode=""></image></view>
		</swiper-item>
		<swiper-item>
			<view class="swiper-item"><image class="swiper-img" src="../../static/img/banner2.jpg" mode=""></image></view>
		</swiper-item>
		<swiper-item>
			<view class="swiper-item"><image class="swiper-img" src="../../static/img/banner3.jpg" mode=""></image></view>
		</swiper-item>
	</swiper>
</template>

<script>
	
</script>

<style scoped>
	swiper{
		width: 100%;
		height: 350rpx;
	}
	.swiper-img{
		width: 100%;
		height: 350rpx;
	}
	
</style>
