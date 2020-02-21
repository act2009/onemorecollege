<template>
	<!--课程列表-->
	<view class="commondityList">
		<Commondity :dataList="CommondityList"></Commondity>
	</view>
</template>

<script>
	import Commondity from './Commodity.vue'
	export default{
		data(){
			return{
				CommondityList:[
					{
						id:1,
						name:"C/C++Linux服务器开发/后台架构师【零声学院】",
						imgUrl:"../../static/img/course1.jpg",
						cprice:"99.00",
						oprice:"199.00",
					},
					{
						id:2,
						name:"C/C++Linux服务器开发/后台架构师【零声学院】",
						imgUrl:"../../static/img/course2.jpg",
						cprice:"399.00",
						oprice:"599.00",
					},
					{
						id:3,
						name:"C/C++Linux服务器开发/后台架构师【零声学院】",
						imgUrl:"../../static/img/course3.jpg",
						cprice:"99.00",
						oprice:"299.00",
					},
					{
						id:4,
						name:"C/C++Linux服务器开发/后台架构师【零声学院】",
						imgUrl:"../../static/img/course4.jpg",
						cprice:"119.00",
						oprice:"199.00",
					},
				]
			}
		},
		components:{
			Commondity
		}
	}
</script>

<style>
</style>
