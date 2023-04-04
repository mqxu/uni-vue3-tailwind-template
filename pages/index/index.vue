<template>
	<!-- <view class="fixed top-0"> -->
	<status-bar></status-bar>
	<!-- </view> -->

	<view class="flex justify-between mb-2">
		<view>
			<text class="text-cyan-500 font-bold ml-2">我创建的</text>
			<text class="text-gray-600 font-bold mx-2">我加入的</text>
			<text class="text-gray-600 font-bold">我共建的</text>
		</view>
		<view class="text-cyan-500">
			<text class="iconfont-lg icon-add"></text>
			<text class="iconfont-lg icon-scan mx-2"></text>
		</view>
	</view>

	<search-box></search-box>

	<template v-for="course in courses" :key="course.courseId">
		<course-item :course="course"></course-item>
	</template>
</template>

<script setup>
	import {
		reactive
	} from 'vue'

	const courses = reactive([{
			courseId: 1,
			courseClass: "软件2242 Web2班",
			courseName: "后端工程开发",
			courseNo: "2942577",
			courseCover: "/static/images/springboot.jpg",
			courseTeacher: {
				name: "许莫淇",
				avatar: "/static/images/me.jpg",
			},
			semester: "2022-2023-2",
			finished: false,
			show: false,
		},
		{
			courseId: 2,
			courseClass: "软件2242 Web2班",
			courseName: "前端工程开发",
			courseNo: "9488275",
			courseCover: "/static/images/vue.jpg",
			courseTeacher: {
				name: "许莫淇",
				avatar: "/static/images/me.jpg",
			},
			semester: "2022-2023-2",
			finished: false,
			show: false,
		},
		{
			courseId: 3,
			courseClass: "软件2242 Web2班",
			courseName: "Web 应用开发",
			courseNo: "8175074",
			courseCover: "/static/images/web.jpg",
			courseTeacher: {
				name: "许莫淇",
				avatar: "./assets/images/me.jpg",
			},
			semester: "2022-2023-2",
			finished: true,
			show: false,
		},
		{
			courseId: 4,
			courseClass: "软件2211班",
			courseName: "Java 程序设计",
			courseNo: "2942526",
			courseCover: "/static/images/java.jpg",
			courseTeacher: {
				name: "许莫淇",
				avatar: "./assets/images/me.jpg",
			},
			semester: "2021-2022-1",
			finished: true,
			show: false,
		},
		{
			courseId: 5,
			courseClass: "软件2136班",
			courseName: "Docker 容器化技术",
			courseNo: "2942536",
			courseCover: "/static/images/docker.png",
			courseTeacher: {
				name: "许莫淇",
				avatar: "./assets/images/me.jpg",
			},
			semester: "2021-2022-1",
			finished: true,
			show: false,
		},
		{
			courseId: 6,
			courseClass: "软件2146班",
			courseName: "React 开发",
			courseNo: "2942546",
			courseCover: "/static/images/react.png",
			courseTeacher: {
				name: "许莫淇",
				avatar: "./assets/images/me.jpg",
			},
			semester: "2021-2022-1",
			finished: true,
			show: false,
		},
	]);
</script>

<style scoped>
	.nav-bar {
		height: 44px;
	}
</style>