<script setup>


</script>

<template>
	<view class="commonTitle-box">
		<div class="title">
			<slot name="name"></slot>
		</div>
		<div class="theme">
			<slot name="theme"></slot>
		</div>
	</view>
</template>


<style lang="scss" scoped>
.commonTitle-box{
	display: flex;
	align-items: center;
	justify-content: space-between;
	padding:36rpx;
	.title{
		font-size:38rpx;
		font-weight: 800;;
	}
}
</style>