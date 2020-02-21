<template>
	<!--横向单个商品组件列表展示,进行数据传递展示-->
	<view class="singleCommodityList">
		<SingleCommodity :dataList="singleCommodityList"></SingleCommodity>
	</view>
</template>

<script>
	import SingleCommodity from './SingleCommodity.vue'
	export default{
		data(){
			return{
				singleCommodityList:[
					{
						id:1,
						imgUrl:"../../static/img/SingleCommodity1.png",
						name:"2020年投资生猪产业策略10讲",
						cprice:"99.00",
						oprice:"199.00",
					    purchased:653,
						description:"1让你抓住未来3年最赚钱机会的一堂课"
					},
					{
						id:1,
						imgUrl:"../../static/img/SingleCommodity1.png",
						name:"2020年投资生猪产业策略10讲2020年投资生猪产业策略10讲2020年投资生猪产业策略10讲",
						cprice:"59.00",
						oprice:"99.00",
						 purchased:151,
						description:"2让你抓住未来3年最赚钱机会的一堂课"
					},
					{
						id:1,
						imgUrl:"../../static/img/SingleCommodity1.png",
						name:"2020年投资生猪产业策略10讲2020年投资生猪产业策略10讲2020年投资生猪产业策略10讲",
						cprice:"99.00",
						oprice:"199.00",
						 purchased:653,
						description:"3让你抓住未来3年最赚钱机会的一堂课"
					},
					{
						id:1,
						imgUrl:"../../static/img/SingleCommodity1.png",
						name:"2020年投资生猪产业策略10讲2020年投资生猪产业策略10讲2020年投资生猪产业策略10讲",
						cprice:"99.00",
						oprice:"199.00",
						 purchased:900,
						description:"4让你抓住未来3年最赚钱机会的一堂课4让你抓住未来3年最赚钱机会的一堂课4让你抓住未来3年最赚钱机会的一堂课4让你抓住未来3年最赚钱机会的一堂课4让你抓住未来3年最赚钱机会的一堂课"
					}
				]
			}
		},
		components:{
			SingleCommodity
		}
	}
</script>

<style>
</style>
