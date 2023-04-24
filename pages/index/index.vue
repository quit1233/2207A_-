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
						<navigator url="/pages/search/search">
							<input type="text" placeholder="请输入内容"/>
							<image src="../../static/ICON/3.png" mode=""></image>
						</navigator>
					</view>
			</view>
		</view>
		<!-- 导航列表 -->
		<view class="list_box">
			<navigator url="/pages/list/list" v-for="(val,key) in menu" :key="'menu_'+key">
				<view>
					<image :src="val.pic" mode=""></image>
					<text>{{val.text}}</text>
				</view>
			</navigator>
<!-- 			<navigator url="/pages/list/list">
				<view>
					<image src="../../static/ICON/7.png" mode=""></image>
					<text>名厨</text>
				</view>
			</navigator>
			<navigator url="/pages/list/list">
				<view>
					<image src="../../static/ICON/4.png" mode=""></image>
					<text>坝坝宴</text>
				</view>
			</navigator>
			<navigator url="/pages/list/list">
				<view>
					<image src="../../static/ICON/6.png" mode=""></image>
					<text>餐饮周边</text>
				</view>
			</navigator> -->
			
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
					<image src="../../static/ICON/man2.jpg" mode=""></image>
					<text>王大牛</text>
				</view>
				<view>
					<image src="../../static/ICON/man3.jpg" mode=""></image>
					<text>斯塔克</text>
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
			<!-- 头部 -->
			<view class="dingbu">
				<image src="../../static/ICON/10.png" mode=""></image>
			</view>
			<!-- 中间 -->
			<view class="canyan_xiangqing">
				<swiper class="swiper"
					:circular = 'true'
					:indicator-dots="indicatorDots" 
					:autoplay="autoplay" 
					:interval="interval"
					:duration="duration"
					indicator-active-color="#fd8d16">
						<swiper-item>
							<view class="zuo">
								<image src="../../static/ICON/goods4.png" mode=""></image>
								<text>盛夏海鲜家宴</text>
								<text style="color: brown;">￥4999/桌</text>
							</view>
							<view class="you">
								<image src="../../static/ICON/goods3.jpg" mode=""></image>
								<text>精品西式家宴</text>
								<text style="color: brown;">￥1299/桌</text>
							</view>
						</swiper-item>
						<swiper-item>
							<view class="zuo">
								<image src="../../static/ICON/goods4.png" mode=""></image>
								<text>盛夏海鲜家宴</text>
								<text style="color: brown;">￥4999/桌</text>
							</view>
							<view class="you">
								<image src="../../static/ICON/goods3.jpg" mode=""></image>
								<text>精品西式家宴</text>
								<text style="color: brown;">￥1299/桌</text>
							</view>
						</swiper-item>
				</swiper>
			</view>
			<!-- 尾部 -->
			<view class="canyan_gengduo">
				<text>更多餐宴</text>
			</view>
		</view>
		<!-- 分割线 -->
		<view class="division"></view>
		<!-- 保证 -->
		<view class="baozheng">
			<!-- 上面 -->
			<view class="baozheng_shangmian">
				<!-- 左边盒子 -->
				<view style="border-right: 1rpx solid #999;">
					<!-- 左边中间盒子 -->
					<view>
						<view class="yyy">
							<image src="../../static/ICON/13.png" mode=""></image>
						</view>
						<view class="eee">
							<text style="font-weight: 800;">信用保障</text>
							<text>服务到位，时间准时</text>
						</view>
					</view>
					
				</view>
				<!-- 右边盒子 -->
				<view>
					<!-- 左边中间盒子 -->
					<view>
						<view class="yyy">
							<image src="../../static/ICON/14.png" mode=""></image>
						</view>
						<view class="eee">
							<text style="font-weight: 800;">认证服务商</text>
							<text>厨师实名，服务可靠</text>
						</view>
					</view>
				</view>
			</view>
			<!-- 下面 -->
			<view class="baozheng_shangmian" style="border-top: 1rpx solid #999;">
				<!-- 左边盒子 -->
				<view style="border-right: 1rpx solid #999;">
					<!-- 左边中间盒子 -->
					<view>
						<view class="yyy">
							<image src="../../static/ICON/15.png" mode=""></image>
						</view>
						<view class="eee">
							<text style="font-weight: 800;">品质服务</text>
							<text>知名品牌，星级厨师</text>
						</view>
					</view>
					
				</view>
				<!-- 右边盒子 -->
				<view>
					<!-- 左边中间盒子 -->
					<view>
						<view class="yyy">
							<image src="../../static/ICON/16.png" mode=""></image>
						</view>
						<view class="eee">
							<text style="font-weight: 800;">安全保障</text>
							<text>全平台在线支付</text>
						</view>
					</view>
				</view>
			</view>
		</view>
		<!-- 分割线 -->
		<view class="division"></view>
		<!-- 管理团队 -->
		<view class="tuandui">
			<image src="../../static/ICON/gg.jpg" mode=""></image>
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
		created(){
			this.getNav()
		},
		onLoad() {

		},
		methods: {
			getNav(){
				uni.request({
					url:'http://api.brqc.com.cn/cpz/shxmp/navlist',
					data:{},
					success:(res)=>{
						console.log(res.data);
						this.menu = res.data.data
					},
					error:(err)=>{
						console.log(err)
					}
				})
			}
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
			// background-color: aqua;
			position:relative;
			// 轮播图
			.banner{
				width: 100%;
				height: 380rpx;
				// background-color: blanchedalmond;
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
			// background-color: chartreuse;
			margin: 20rpx auto;
			display: flex;
			justify-content:space-between;
			view{
				width: 125rpx;
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
					font-size: 30rpx;
					font-weight: 550;
					color: #333;
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
						border-radius: 50%;
					}
					text{
						margin: 0 auto;
						margin-top: 18rpx;
						font-weight: 550;
						font-size: 35rpx;
						color: #333;
					}
				}
			}
			.mingchu{
				width: 100%;
				height: 40rpx;
				// background-color: aqua;
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
			background-color: #fff;
			padding-top: 40rpx;
			// 头部
			.dingbu{
				width: 460rpx;
				height: 40rpx;
				// background-color: antiquewhite;
				margin: 0 auto;
				image{
					width: 100%;
					height: 100%;
				}
			}
			// 中间
			.canyan_xiangqing{
				width: 92%;
				height: 321rpx;
				// background-color: brown;
				margin: 0 auto;
				margin-top: 40rpx;
				
				.swiper{
					width: 100%;
					height: 370rpx;
					swiper-item{
						width: 100%;
						height: 100%;
						// background-color: antiquewhite;
						display: flex;
						justify-content:space-between;
						
						.zuo{
							width: 46%;
							height: 320rpx;
							// background-color: burlywood;
							display: flex;
							flex-direction:column;
							border-radius: 15rpx;
							box-shadow: 5px 5px 4px rgba(0, 0, 0, 0.1);
							image{
								width: 100%;
								height: 200rpx;
								border-radius: 15rpx;
								
							}
							text{
								margin-top: 10rpx;
								font-weight: 800;
								margin-left: 15rpx;
							}
						}
						.you{
							width: 46%;
							height: 320rpx;
							// background-color: burlywood;
							display: flex;
							flex-direction:column;
							border-radius: 15rpx;
							box-shadow: 5px 5px 4px rgba(0, 0, 0, 0.1);
							image{
								width: 100%;
								height: 200rpx;
								border-radius: 15rpx;
							}
							text{
								margin-top: 10rpx;
								font-weight: 800;
								margin-left: 15rpx;
							}
						}
					}
				}
			}
			// 尾部
			.canyan_gengduo{
				width: 100%;
				height: 40rpx;
				// background-color: blue;
				margin-top: 50rpx;
				display: flex;
				flex-direction:column;
				
				text{
					margin: 0 auto;
				}
			}
		}
		// 保证盒子
		.baozheng{
			width: 100%;
			height: 350rpx;
			// background-color: darkgrey;
			padding-bottom: 20rpx;
			// 上面盒子
			.baozheng_shangmian{
				width: 100%;
				height: 175rpx;
				// background-color: aquamarine;
				display: flex;
				// 左边盒子大盒子
				view{
					width: 50%;
					height: 175rpx;
					// background-color: bisque;
					// 左边盒子里面盒子
					view{
						width: 96%;
						height: 75rpx;
						// background-color: blueviolet;
						margin: 0 auto;
						margin-top: 22rpx;
						display: flex;
						// 左边中间盒子
						.yyy{
							width: 80rpx;
							height: 80rpx;
							// background-color: darkorange;
							image{
								width: 80rpx;
								height: 80rpx;
							}
						}
						.eee{
							width: 300rpx;
							height: 90rpx;
							// background-color: darkviolet;
							display: flex;
							flex-direction:column;
							margin-left: 7rpx;
							text{
								font-size: 30rpx;
							}
						}
						
					}
				}
			}
		}
		// 管理团队
		.tuandui{
			width: 100%;
			height: 430rpx;
			background-color: #fff;
			image{
				width: 100%;
				height: 390rpx;
			}
		}
	}
</style>
