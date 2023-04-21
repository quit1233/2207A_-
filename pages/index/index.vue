<template>
	<view class="box">
		<!-- 头部 -->
		<view class="head">
			<!-- 轮播图 -->
			<view class="banner">
				<swiper class="swiper"
					:circular = 'true'
					:indicator-dots="indicatorDots" 
					:autoplay="autoplay" 
					:interval="interval"
					:duration="duration"
					indicator-active-color="#fd8d16">
						<swiper-item>
							<image src="../../static/ICON/banner.png"></image>
						</swiper-item>
						<swiper-item>
							<image src="../../static/ICON/banner.png"></image>
						</swiper-item>
						<swiper-item>
							<image src="../../static/ICON/banner.png"></image>
						</swiper-item>
				</swiper>
			</view>
			<!-- 搜索框 -->
			<view class="search_box">
				<view class="search">
					<input type="text" placeholder="请输入内容"/>
					<image src="../../static/ICON/3.png" mode=""></image>
				</view>
			</view>
		</view>
		<!-- 导航列表 -->
		<view class="list_box">
			<navigator url="/pages/list/list">
				<view>
					<image src="../../static/ICON/5.png" mode=""></image>
					<text>搜索</text>
				</view>
			</navigator>
			<navigator url="/pages/list/list">
				<view>
					<image src="../../static/ICON/5.png" mode=""></image>
					<text>搜索</text>
				</view>
			</navigator>
			<navigator url="/pages/list/list">
				<view>
					<image src="../../static/ICON/5.png" mode=""></image>
					<text>搜索</text>
				</view>
			</navigator>
			<navigator url="/pages/list/list">
				<view>
					<image src="../../static/ICON/5.png" mode=""></image>
					<text>搜索</text>
				</view>
			</navigator>

		</view>
		<!-- 广告 -->
		<view class="advertising">
			<image src="../../static/ICON/8.png" mode=""></image>
		</view>
		<!-- 分割线 -->
		<view class="division"></view>
		<!-- 优选名厨大盒子 -->
		<view class="famous_chef">
			<!-- 头部 -->
			<view class="famous_chef_tou">
				<image src="../../static/ICON/9.png" mode=""></image>
			</view>
			<!-- 详情 -->
			<view class="famous_chef_xiangqing">
				<view>
					<image src="../../static/ICON/man1.jpg" mode=""></image>
					<text>张小妹</text>
				</view>
				<view>
					<image src="../../static/ICON/man1.jpg" mode=""></image>
					<text>张小妹</text>
				</view>
				<view>
					<image src="../../static/ICON/man1.jpg" mode=""></image>
					<text>张小妹</text>
				</view>
			</view>
			<view class="mingchu">
				<text>更多名厨</text>
			</view>
		</view>
		<!-- 分割线 -->
		<view class="division"></view>
		<!-- 优选餐宴 -->
		<view class="canyan">
			<view class="dingbu">
				<image src="../../static/ICON/10.png" mode=""></image>
			</view>
			
			
		</view>
		
	</view>
</template>

<script>
	export default {
		data() {
			return {
				indicatorDots: true,
				autoplay: true,
				interval: 2000,
				duration: 500,
				menu:[]
			}
		},
		onLoad() {

		},
		methods: {

		}
	}
</script>

<style lang="less">
	*{
	    /* 内边框 */
	    padding: 0;
	    /* 外边框 */
	    margin: 0;
	    /* 不改变盒子大小 */
	    box-sizing: border-box;
	}
	// 最大盒子
	.box{
		width: 100%;
		// 头部盒子
		.head{
			width: 100%;
			height: 443rpx;
			background-color: aqua;
			position:relative;
			// 轮播图
			.banner{
				width: 100%;
				height: 380rpx;
				background-color: blanchedalmond;
				.swiper{
					width: 100%;
					height: 380rpx;
					swiper-item{
						image{
							display: block;
							width: 100%;
							height: 380rpx;
						}
					}
				}
			}
			// 搜索框盒子
			.search_box{
				width: 100%;
				height: 90rpx;
				// background-color: chartreuse;
				position: absolute;
				top: 330rpx;
				// 搜索
				.search{
					width: 86%;
					height: 90rpx;
					background-color: #fff;
					border-radius: 50rpx;
					margin: 0 auto;
					padding-top: 20rpx;
					padding-left: 30rpx;
					position: relative;
					box-shadow: 5px 8px 8px rgba(0, 0, 0, 0.1);
					input{
					}
					// 搜索图片
					image{
						display: block;
						position: absolute;
						top: 27rpx;
						right: 30rpx;
						width: 35rpx;
						height: 35rpx;
						
					}
				}
			}
		}
		// 导航列表
		.list_box{
			width: 88%;
			height: 155rpx;
			background-color: chartreuse;
			margin: 20rpx auto;
			display: flex;
			justify-content:space-between;
			view{
				width: 113rpx;
				height: 155rpx;
				// background-color: coral;
				display: flex;
				flex-direction: column;
				image{
					width: 113rpx;
					height: 113rpx;
					margin: 0 auto;
				}
				text{
					margin: 0 auto;
				}
			}
		}
		// 广告
		.advertising{
			width: 96%;
			height: 300rpx;
			background-color: blue;
			margin: 35rpx auto;
			image{
				width: 100%;
				height: 300rpx;
			}
		}
		// 分割线
		.division{
			width: 100%;
			height: 20rpx;
			background-color: #eee;
		}
		// 优选名厨
		.famous_chef{
			width: 96%;
			height: 509rpx;
			// background-color: antiquewhite;
			margin: 0 auto;
			padding-top: 30rpx;
			// 头部
			.famous_chef_tou{
				width: 460rpx;
				height: 85rpx;
				// background-color: aqua;
				margin: 0 auto;
				image{
					width: 100%;
					height: 100%;
				}
			}
			.famous_chef_xiangqing{
				width: 94%;
				height: 255rpx;
				// background-color: chartreuse;
				margin: 0 auto;
				margin-top: 35rpx;
				display: flex;
				justify-content:space-between;
				
				view{
					width: 217rpx;
					height: 100%;
					background-color: #fff;
					padding-top: 24rpx;
					display: flex;
					flex-direction:column;
					box-shadow: 0px 0px 4px rgba(0, 0, 0, 0.4);
					border-radius: 8rpx;
					image{
						width: 110rpx;
						height: 110rpx;
						margin: 0 auto;
					}
					text{
						margin: 0 auto;
						margin-top: 18rpx;
						font-weight: 500;
						font-size: 35rpx;
					}
				}
			}
			.mingchu{
				width: 100%;
				height: 40rpx;
				background-color: aqua;
				margin-top: 35rpx;
				display: flex;
				flex-direction:column;
				
				text{
					margin: 0 auto;
				}
			}
		}
		// 优选餐宴
		.canyan{
			width: 100%;
			height: 555rpx;
		}
	}
</style>
