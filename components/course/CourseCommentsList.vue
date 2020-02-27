<template>
<!-- 	查看更多-课程全部评论 -->
	<view class="coursecommentsList">

	<Card
	cardTitle="全部评论"
	fontSize="30rpx"
	paddingData="0"></Card>
		<Comments :dataList="CommentsList"></Comments>

	</view>
</template>

<script>
	import Card         from '@/components/common/Card.vue'
	import Comments     from '@/components/common/Comments.vue'
	export default{
		data(){
			return{
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
			Card,
			Comments 
		}
	}
</script>

<style>
</style>
