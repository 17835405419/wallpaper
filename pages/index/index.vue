<script setup>

</script>

<template>
	<view class="home-layout">
		<div class="banner-box">
			<swiper indicator-dots :autoplay="true" :circular="true" :interval="2000" indicator-color="#c0c0c0"
				indicator-active-color="#ffffff">
				<swiper-item>
					<image src="../../common/images/banner1.jpg" mode=""></image>
				</swiper-item>
				<swiper-item>
					<image src="../../common/images/banner2.jpg" mode=""></image>
				</swiper-item>
				<swiper-item>
					<image src="../../common/images/banner3.jpg" mode=""></image>
				</swiper-item>
			</swiper>
		</div>
		<div class="noticeLists-box">
			<div class="left">
				<uni-icons type="sound" size="24" color=" #2ba886"></uni-icons>
				<text class="title">公告</text>
			</div>
			<div class="center">
				<swiper :autoplay="true" :interval="2000" :vertical="true">
					<swiper-item v-for="item in 3">
						<view class="notice-content">啦啦啦啦啦啦啦啦啦啦啦啦啦啦啦啦啦啦啦啦</view>
					</swiper-item>
				</swiper>
			</div>
			<div class="right">
				<uni-icons type="right" size="21"></uni-icons>
			</div>
		</div>
	
		<div class="select">
			<CommonTitle>
				<template #name>
					每日推荐
				</template>
				<template  #theme>
					<view>啦啦啦啦</view>
				</template>
			</CommonTitle>
			<div class="scroll">
				<scroll-view scroll-x  :scroll-left="true">
					<image src="../../common/images/preview_small.webp" mode="aspectFill" ></image>
					<image src="../../common/images/preview1.jpg" mode=""></image>
					<image src="../../common/images/preview2.jpg" mode=""></image>	
					<image src="../../common/images/preview_small.webp" mode=""></image>
					<image src="../../common/images/preview1.jpg" mode=""></image>
					<image src="../../common/images/preview2.jpg" mode=""></image>	
				</scroll-view>
			</div>
		</div>
	
	</view>
</template>

<style lang="scss" scoped>
	.banner-box {
		width: 750rpx;
		height: 336rpx;

		swiper {
			width: 700rpx;
			height: 100%;
			margin: 0 auto;

			&-item {
				width: 100%;
				height: 100%;

				image {
					width: 100%;
					height: 100%;
				}
			}
		}
	}

	.noticeLists-box {
		box-sizing: border-box;
		display: flex;
		align-items: center;
		justify-content: space-between;
		width: 700rpx;
		height: 79rpx;
		background-color: #f9f9f9;
		border-radius: 40rpx;
		margin: 20rpx auto;
		padding: 0 30rpx;
		font-size: 24rpx;

		.left {
			display: flex;
			align-items: center;

			.title {
				font-weight: 800;
				color: #2ba886;
			}
		}

		.center {
			flex: 1;
			height: 100%;

			swiper {
				height: 100%;
				padding: 0 30rpx;

				&-item {
					height: 100%;
					display: flex;
					align-items: center;
					font-size: 24rpx;
					.notice-content{
						white-space: nowrap;
						overflow: hidden;
						text-overflow: ellipsis;
					}
				
				}
			}
		}

	}
	.scroll{
		white-space: nowrap;
		padding-left: 30rpx;
		scroll-view{
			image{
				height: 442rpx;
				width: 200rpx;
				margin-right:15rpx;
				border-radius: 15rpx;
				&:last-child{
					margin-right:30rpx;
				}
			}
		}
	
	}
</style>