<template>
	<!--头部课程图片与标题-->
	<view class="intro">
		
	<view class="intro-content"
	v-for="(item,index) in dataList" 
	:key="index">
	
		{{item.intro}}
			
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

<style>
</style>
