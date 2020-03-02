<template>
	<!--我的学习/收藏课程-->
	<view class="collection">
      		<Card cardTitle="我的学习"></Card>
		<SingleCommodity :dataList="collection"></SingleCommodity>
	</view>
</template>

<script>
	import SingleCommodity from '@/components/common/SingleCommodity.vue'
	import Card            from '@/components/common/Card.vue'
	export default{
		data(){
			return{
				collection:[
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
			SingleCommodity,
			Card
		}
	}
</script>

<style scoped>

</style>
