<template>
	<view :style="{ height: barHeight }" class="uni-status-bar">
		<slot></slot>
	</view>
</template>

<script setup>
	import { ref } from 'vue'
	const statusBarHeight = uni.getSystemInfoSync().statusBarHeight + 'px';
	const barHeight = ref(statusBarHeight);
</script>

<style scoped>
	.uni-status-bar {
		width: 750rpx;
		background-color: var(--light);
	}
</style>