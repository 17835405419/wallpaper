<script setup>
	
</script>

<template>
	<view class="classfily pageBg">
		<view class="themeCard" v-for="item in 12">
			<ThemeCard></ThemeCard>
		</view>
	</view>
</template>

<style lang="scss" scoped>
	.classfily{
		padding:0 30rpx;
		display: grid;
		gap: 15rpx;
		grid-template-columns: repeat(3,1fr);
	}
</style>
