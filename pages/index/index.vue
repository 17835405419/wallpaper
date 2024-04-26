<script setup>

</script>

<template>
	<view class="home-layout">
		<view class="banner-box">
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
		</view>
		<view class="noticeLists-box">
			<view class="left">
				<uni-icons type="sound" size="24" color=" #2ba886"></uni-icons>
				<text class="title">公告</text>
			</view>
			<view class="center">
				<swiper :autoplay="true" :interval="2000" :vertical="true">
					<swiper-item v-for="item in 3">
						<view class="notice-content">啦啦啦啦啦啦啦啦啦啦啦啦啦啦啦啦啦啦啦啦</view>
					</swiper-item>
				</swiper>
			</view>
			<view class="right">
				<uni-icons type="right" size="21"></uni-icons>
			</view>
		</view>
	
		<view class="select">
			<CommonTitle>
				<template #name>
					每日推荐
				</template>
				<template  #theme>
					<view class="calendar">
						<uni-icons type="calendar" size="24" 	color="#2ba886"></uni-icons>
						<uni-dateformat class="time" :date="Date.now()" format="dd日"></uni-dateformat>
					</view>
				</template>
			</CommonTitle>
			<view class="scroll">
				<scroll-view scroll-x  :scroll-left="true">
					<image src="../../common/images/preview_small.webp" mode="aspectFill" ></image>
					<image src="../../common/images/preview1.jpg" mode=""></image>
					<image src="../../common/images/preview2.jpg" mode=""></image>	
					<image src="../../common/images/preview_small.webp" mode=""></image>
					<image src="../../common/images/preview1.jpg" mode=""></image>
					<image src="../../common/images/preview2.jpg" mode=""></image>	
				</scroll-view>
			</view>
		</view>
	
		<view class="special-sbject">
			<CommonTitle>
				<template #name>
					专题精选
				</template>
				<template  #theme>
					<navigator  class="more">
						More+
					</navigator>
				</template>
			</CommonTitle>
			<view class="themeCard" >
				<view class="item" v-for="item in 8">
					<ThemeCard></ThemeCard>
				</view>
				<ThemeCard :isMore="true"></ThemeCard>
			</view>
			
		</view>
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
	.select{
		font-size:30rpx;
		.calendar{
			display: flex;
			align-items: center;
			color:#2ba886;
			.time{
				margin-left: 10rpx;
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
	.special-sbject{
		.more{
			font-size: 36rpx;
			color:#868686;
		}
		.themeCard{
			padding: 30rpx;
			display: grid;
			gap: 15rpx;
			grid-template-columns: repeat(3,1fr);
		}
	}

</style>