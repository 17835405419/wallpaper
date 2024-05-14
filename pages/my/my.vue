<script setup>

</script>

<template>
	<view class="my-box pageBg">
		<view class="userInfo">
			<view class="avater">
				<image src="../../static/images/xxmLogo.png" mode=""></image>
			</view>
			<view class="ip">
				100.100.100.100
			</view>
			<view class="address">
				来自于：山东
			</view>
		</view>
		<view class="section">
			<view class="list">
				<view class="row">
					<view class="left">
						<uni-icons type="download-filled" size="20"></uni-icons>
						<view class="text">
							我的下载
						</view>
					</view>
					<view class="right">
						<view class="text">
							0
						</view>
						<uni-icons type="right" size="15"></uni-icons>
					</view>
				</view>
				<view class="row">
					<view class="left">
						<uni-icons type="star-filled" size="20"></uni-icons>
						<view class="text">
							我的评分
						</view>
					</view>
					<view class="right">
						<view class="text">
							33
						</view>
						<uni-icons type="right" size="15"></uni-icons>
					</view>
				</view>
				<!-- TODO 客服功能暂未实现 -->
				<view class="row">
					<view class="left">
						<uni-icons type="weixin" size="20"></uni-icons>
						<view class="text">
							联系客服
						</view>
					</view>
					<view class="right">
						<view class="text">
							0
						</view>
						<uni-icons type="right" size="15"></uni-icons>
					</view>
				</view>
			</view>
		</view>
		<view class="section">
			<view class="list">
				<view class="row">
					<view class="left">
						<uni-icons type="notification-filled" size="20"></uni-icons>
						<view class="text">
							订阅更新
						</view>
					</view>
					<view class="right">
						<view class="text">
							33
						</view>
						<uni-icons type="right" size="15"></uni-icons>
					</view>
				</view>
				<view class="row">
					<view class="left">
						<uni-icons type="flag-filled" size="20"></uni-icons>
						<view class="text">
							常见问题
						</view>
					</view>
					<view class="right">
						<view class="text">
							33
						</view>
						<uni-icons type="right" size="15"></uni-icons>
					</view>
				</view>
			</view>
		</view>
	</view>
</template>

<style lang="scss" scoped>
	.my-box {
		.userInfo {
			display: flex;
			align-items: center;
			justify-content: center;
			flex-direction: column;
			padding: 50rpx 0;

			.avater {
				width: 160rpx;
				height: 160rpx;
				border-radius: 50%;
				overflow: hidden;

				image {
					width: 100%;
					height: 100%;
				}
			}

			.ip {
				font-size: 44rpx;
				color:$text-font-color-1;
				padding: 20rpx 0 5rpx;

			}

			.address {
				font-size: 28rpx;
				color: $text-font-color-3;
			}
		}

		.section {
			width: 690rpx;
			margin: 50rpx auto;
			border: 1px solid $border-color;
			border-radius: 10rpx;
			box-shadow: 0 0 30rpx rgba(0, 0, 0, 0.05);
			background-color: #fff;

			.list {
				.row {
					display: flex;
					justify-content: space-between;
					align-content: center;
					padding: 0 30rpx;
					height: 100rpx;
					border-bottom: 1px solid $border-color;
					font-size: 26rpx;

					&:last-child {
						border-bottom: 0;
					}

					.left {
						display: flex;
						align-items: center;

						:deep() {
							.uni-icons {
								color: $brand-theme-color !important;
							}
						}

						.text {
							padding-left: 20rpx;
							color:$text-font-color-2;
						}
					}

					.right {
						display: flex;
						align-items: center;

						.text {
							padding-left: 15rpx;
							color:$text-font-color-4;
							padding-right: 10rpx;
						} 
					}
				}
			}
		}
	}
</style>