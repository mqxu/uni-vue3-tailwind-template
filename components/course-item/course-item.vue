<template>
	<!-- 每门课程分为：上中下三部分 -->
	<view class="border-bottom bg-white mb-2 py-2 px-2">
		<!-- 上：班课名称 -->
		<text class="text-gray-700 font-bold px-2">{{course.courseName}}</text>

		<!-- 中：左中右结构  -->
		<view class="flex px-2 mt-1">
			<!-- 左-班课图 -->
			<view class="flex-1">
				<image :src="course.courseCover" class="w-16 h-16 rounded-lg"></image>
			</view>

			<!-- 中： 上下结构 班级 + 学期、班课号 -->
			<view class="flex-4 ml-2">
				<text>{{course.courseClass}}</text>
				<view class="mt-2">
					<text class="text-gray-400 mr-2">{{course.semester}}</text>
					<text class="text-cyan-500">{{course.courseNo}}</text>
				</view>
			</view>

			<!-- 右：箭头 -->
			<view class="flex-1 text-right">
				<navigator :url="'/pages/course/course?item='+ encodeURIComponent(JSON.stringify(course))">
					<text class="iconfont icon-right text-gray-400"></text>
				</navigator>
			</view>
		</view>

		<!-- 下方的几组图标+文字 -->
		<!-- <view class="p-2 f-around text-center text-gray-400">
			<view class="flex flex-column">
				<text class="iconfont icon-selected"></text>
				<text class="font-sm  mt-1">签到</text>
			</view>
			<view class="flex flex-column">
				<text class="iconfont icon-pepole"></text>
				<text class="font-sm  mt-1">课堂</text>
			</view>
			<view class="flex flex-column">
				<text class="iconfont icon-fillin"></text>
				<text class="font-sm  mt-1">课件</text>
			</view>
			<view class="flex flex-column">
				<text class="iconfont icon-gift"></text>
				<text class="font-sm  mt-1">活动</text>
			</view>
			<view class="flex flex-column">
				<text class="iconfont icon-voice text-info"></text>
				<text class="font-sm  mt-1">语音</text>
			</view>
		</view>
 -->
	</view>
</template>

<script setup>
	const props = defineProps({
		course: Object
	})
</script>