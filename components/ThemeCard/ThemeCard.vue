<script setup>
import {defineProps} from "vue" 
defineProps({
	isMore:{
		type:Boolean,
		default:false
	}
})
</script>

<template>
	<navigator url="" class="themeCard-box" v-if="!isMore"> 
		<image class="pic" src="../../common/images/classify1.jpg" mode=""></image>
		<view class="theme-title">可爱萌宠</view>
		<view class="time-notice">
			三天前更新
		</view>
	</navigator>
	<navigator url="" class="themeCard-box more" v-else>
		<image class="pic" src="../../common/images/more.jpg" mode=""></image>
		<view class="mask">
			<uni-icons type="more-filled" size="34" color="#fff"></uni-icons>
			<view class="text">
				更多
			</view>
		</view>
		
	</navigator>
	
</template>


<style lang="scss" scoped>
.themeCard-box{
	height: 340rpx;
	position: relative;
	border-radius: 15rpx;
	overflow: hidden;
	.pic{
		height: 100%;
		width: 100%;
	}
	.theme-title{
		position: absolute;
		bottom: 0;
		left: 0;
		height: 70rpx;
		width: 100%;
		background-color: rgba(0,0,0,0.2);
		backdrop-filter: blur(20rpx);
		display: flex;
		align-items: center;
		justify-content: center;
		color: #fff;
	}
	.time-notice{
		background-color: #f29e84;
		font-size: 22rpx;
		padding: 15rpx;
		position: absolute;
		top: 0;
		color: #fff;
		transform: scale(0.8);
		transform-origin: top left;
		border-radius: 0 0 15rpx 0;
	}
}

.more{
	position: relative;
	.mask{
		height: 100%;
		width: 100%;
		position: absolute;
		left: 0;
		bottom: 0;
		background-color: rgba(0,0,0,0.2);
		backdrop-filter: blur(20rpx);
		display: flex;
		flex-direction: column;
		align-items: center;
		justify-content: center;
		color: #fff;
	}
}
</style>