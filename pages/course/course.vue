<template>
	<view class="course">
<!-- 		<PostData></PostData> -->
			<Header :dataList="CourseHeader"></Header>
		<section class="Index-Page">
		  <s-tabs :effect="true" v-model="activeTab" @change="change" :nav-per-view="3">
		    <s-tab title="<span>简介</span>">
			<view class="paddingtop36">
	          	<CourseIntro :dataList="CourseIntroduction"></CourseIntro >
	       </view>
			</s-tab>
			
		    <s-tab title="<span>目录</span>">
			<view class="">
             <CourseItems :dataList="videoItems"></CourseItems>
		    </view>
			</s-tab>
			
		    <s-tab title="<span>评价</span>">
			<view class="paddingtop36">
			
			<Card 
			cardTitle="课程评论"
			goName="查看更多" 
			fontSize="30rpx"
			paddingData="0"></Card>
			
			<Comments :dataList="CommentsList"></Comments>
		    </view>
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
	import CourseItems  from '@/components/course/CourseItems.vue'
	import Card         from '@/components/common/Card.vue'
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
					
				],
				CommentsList:[
					{
						id:1,
						userid:256,
						uname:"AllenZhao3",
						avatar:"../../static/img/avatar2.jpg",
						courseid:34,
						to_user_id:0,
						content:"课程有优惠吗？",
						create_time:"2020-02-27"
					},
					{
						id:2,
						userid:0,//0表示[课程团队回复]
						uname:"课程团队回复",
						avatar:"../../static/img/avatar1.jpg",
						courseid:34,
						to_user_id:0,
						content:"你好，现在购买即有优惠活动的！",
						create_time:"2020-02-27"
					},
					{
						id:3,
						userid:256,
						uname:"xixi",
						courseid:34,
						avatar:"../../static/img/avatar2.jpg",
						to_user_id:0,
						content:"听了很多老师的课，最终我觉得还是文豪老师的课是通俗易懂，收益颇多。很感谢他在备课的时候能考虑到如何让我们更好的去理解他所讲的内容。如什么是通货膨胀？人民币贬值对老百姓的影响，行为金融等等。从最开始荔枝微课遇见，一路追随到网易云课堂。文豪金融——感谢感恩有你！",
						create_time:"2020-02-27"
					},
					{
						id:4,
						userid:256,
						courseid:34,
						uname:"xixi",
						avatar:"../../static/img/avatar2.jpg",
						to_user_id:0,
						content:"1",
						create_time:"2020-02-27"
					},
					{
						id:5,
						userid:256,
						courseid:34,
						uname:"xixi",
						avatar:"../../static/img/avatar2.jpg",
						to_user_id:0,
						content:"嘻嘻好😳支持",
						create_time:"2020-02-27"
					}
					
				]

			}
		},
		components:{
			Header,
			sTabs,
			sTab,
			CourseIntro,
			CourseItems,
			Card,
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

</style>
