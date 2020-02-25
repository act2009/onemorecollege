<template>
<!-- 	接受和传递数据 test到各个模块-->
<view class="postdata">
			<CourseIntro :dataList="CourseCourseIntro"></CourseIntro >
</view>

</template>

<script>
	import CourseIntro       from './CourseIntro.vue'
	import sTabs        from '@/components/s-ui/s-tabs/index.vue'
	import sTab         from '@/components/s-ui/s-tab/index.vue'
	export default{
		data(){
			return{
				CourseCourseIntro:[
					{
						imgUrl:"../../static/img/course-intro.jpg",
						name:"来自福布斯精英的25节课",
						description:"让你抓住未来3年最赚钱机会的一堂课让你抓住未来让你抓住未来3年最赚钱机会的一堂课让你抓住未来3年最赚钱机会的一堂课3年最赚钱机会的一堂课让你抓住未来3年最赚钱机会的一堂课让你抓住未来3年最赚钱机会的一堂课让你抓住未来3年最赚钱机会的一堂课"
					},
					
				]
			}
		},
		components:{
			CourseIntro
		}
	}
</script>

<style>
</style>
