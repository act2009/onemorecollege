<template>
	<view class="course">
		<PostData></PostData>
			<Header :dataList="CourseHeader"></Header>
		<section class="Index-Page">
		  <s-tabs :effect="true" v-model="activeTab" @change="change" :nav-per-view="3">
		    <s-tab title="<span>简介</span>">
			<view class="course-intro">
	          	<CourseIntro :dataList="CourseIntroduction"></CourseIntro >
	       </view>

			</s-tab>
		    <s-tab title="<span>目录</span>">
             <Catalog :dataList="videoItems"></Catalog>
			</s-tab>
		    <s-tab title="<span>评价</span>">
			<comments></comments>

			</s-tab>
		  </s-tabs>
		</section>
	</view>
</template>

<script>
	import PostData     from '@/components/course/PostData.vue'
	import Header       from '@/components/course/Header.vue'
	import sTabs        from '@/components/s-ui/s-tabs/index.vue'
	import sTab         from '@/components/s-ui/s-tab/index.vue'
	import CourseIntro  from '@/components/course/CourseIntro.vue'
	import Catalog      from '@/components/common/Catalog.vue'
	import Comments     from '@/components/common/Comments.vue'

	

	export default {
		data() {
			return {
				activeTab: 0,
				CourseIntroduction:[
					{
						intro:"很多喜欢GTA的朋友们相信一定都和我一样在默默期待着GTA6的降临，之前预测了几次GTA6的主城：伦敦？东京？巴黎？都有极大的可能，但是最终还是以官方消息为主，下面的消息证明了我们期待的GTA6是存在的，虽然官方没有透漏消息，但是关于GTA6的动作捕捉新闻流漏了出来。演员Tim Neff在他的简历中透露他进行了《侠盗猎车手6》的动作捕捉。另外他还进行了《荒野大镖客2》的动作捕捉工作。目前《GTA6》还没有官方正式公布。"
					},
					
				],
				CourseHeader:[
					{
						imgUrl:"../../static/img/course-intro.jpg",
						name:"来自福布斯精英的25节课",
						description:"让你抓住未来3年最赚钱机会的一堂课让你抓住未来让你抓住未来3年最赚钱机会的一堂课让你抓住未来3年最赚钱机会的一堂课3年最赚钱机会的一堂课让你抓住未来3年最赚钱机会的一堂课让你抓住未来3年最赚钱机会的一堂课让你抓住未来3年最赚钱机会的一堂课"
					},
					
				],

				// CourseIntro:[
				// 	{
				// 		imgUrl:"../../static/img/course-intro.jpg",
				// 		name:"来自福布斯精英的25节课",
				// 		description:"让你抓住未来3年最赚钱机会的一堂课让你抓住未来让你抓住未来3年最赚钱机会的一堂课让你抓住未来3年最赚钱机会的一堂课3年最赚钱机会的一堂课让你抓住未来3年最赚钱机会的一堂课让你抓住未来3年最赚钱机会的一堂课让你抓住未来3年最赚钱机会的一堂课"
				// 	},
					
				// ],
				videoItems:[
					{
						id:1,
						name:"【视频版】第一章：听得懂的金融思维",
						visible:"可试看"
					},
					{
						id:2,
						name:"【视频版】第二章：“杠杆”是什么？它到底是天使还是魔鬼？",
						visible:"可试看"
					},
					
				]

			}
		},
		components:{
			Header,
			sTabs,
			sTab,
			CourseIntro,
			Catalog,
			Comments,
			PostData

		},
		
		methods: {
    change (index) {
      console.log(index);
    }
		}
	}
</script>

<style scoped>
	.course-intro{
		padding: 36rpx 0;
	}
</style>
