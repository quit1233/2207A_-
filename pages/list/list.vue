<template>
	<view class="box">
		<!-- 搜索框 -->
		<view class="search_box">
			<view class="search">
				<input type="text" placeholder="搜美食，菜谱"/>
				<image src="../../static/ICON/3.png" mode=""></image>
			</view>
		</view>
		<!-- 横线 -->
		<view class="hangxian"></view>
		<!-- 列表 -->
		<view class="list">
			<!-- 左盒子 -->
			<view class="list_zuo">
				<!-- 文字 -->
				<view class="list_zuo_wenzi">
					<text>白酒</text>
				</view>
				<view class="list_zuo_wenzi">
					<text>啤酒</text>
				</view>
				<view class="list_zuo_wenzi">
					<text>红酒</text>
				</view>
				<view class="list_zuo_wenzi">
					<text>饮料</text>
				</view>
			</view>
			<!-- 右盒子 -->
			<view class="list_you">
				<!-- 标题 -->
				<view class="biaoti">白酒</view>
				<!-- 列表 -->
				<view class="list_you_list">
					<!-- 列表左盒子图片和文字 -->
					<view class="list_you_list_wenzi">
						<!-- 图片 -->
						<view class="list_you_list_wenzi_tupian">
							<image src="../../static/ICON/goods2.jpg" mode=""></image>
						</view>
						<!-- 文字 -->
						<view class="list_you_list_wenzi_wenzi">
							<text>贵州茅台</text>
							<text style="color: crimson;">￥100/瓶</text>
						</view>
					</view>
					<!-- 列表右盒子加减 -->
					<view class="list_you_list_jiajian">
						<!-- 图片 -->
						<view class="list_you_list_jiajian_tupian">
							<text>+</text>
						</view>
					</view>
				</view>
				
				<!-- 列表 -->
				<view class="list_you_list">
					<!-- 列表左盒子图片和文字 -->
					<view class="list_you_list_wenzi">
						<!-- 图片 -->
						<view class="list_you_list_wenzi_tupian">
							<image src="../../static/ICON/goods2.jpg" mode=""></image>
						</view>
						<!-- 文字 -->
						<view class="list_you_list_wenzi_wenzi">
							<text>贵州茅台</text>
							<text style="color: crimson;">￥100/瓶</text>
						</view>
					</view>
					<!-- 列表右盒子加减 -->
					<view class="list_you_list_jiajian">
						<!-- 图片 -->
						<view class="list_you_list_jiajian_tupian">
							<text>+</text>
						</view>
					</view>
				</view>
				
				<!-- 列表 -->
				<view class="list_you_list">
					<!-- 列表左盒子图片和文字 -->
					<view class="list_you_list_wenzi">
						<!-- 图片 -->
						<view class="list_you_list_wenzi_tupian">
							<image src="../../static/ICON/goods2.jpg" mode=""></image>
						</view>
						<!-- 文字 -->
						<view class="list_you_list_wenzi_wenzi">
							<text>贵州茅台</text>
							<text style="color: crimson;">￥100/瓶</text>
						</view>
					</view>
					<!-- 列表右盒子加减 -->
					<view class="list_you_list_jiajian">
						<!-- 图片 -->
						<view class="list_you_list_jiajian_tupian">
							<text>+</text>
						</view>
					</view>
				</view>
			</view>
		</view>
		<!-- 加入购物车 -->
		<view class="gwc">
			<!-- 购物车左 -->
			<view class="gwc_zuo">
				<!-- 图片 -->
				<view class="gwc_zuo_tupian">
					<image src="../../static/ICON/icon_car.png" mode=""></image>
				</view>
				<!-- 文字 -->
				<view class="gwc_zuo_wenzi">
					<text>￥200</text>
				</view>
			</view>
			<!-- 购物车右 -->
			<view class="wgc_you">
				<text>购买</text>
			</view>
		</view>
	</view>
</template>

<script>
	export default {
		data() {
			return {
				
			}
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
	.box{
		width: 100%;
		padding-top: 15rpx;
		// 搜索框盒子
		.search_box{
			width: 100%;
			height: 90rpx;
			// background-color: #333;
			// position: absolute;
			top: 330rpx;
			// 搜索
			.search{
				width: 92%;
				height: 90rpx;
				background-color: #f1f1f1;
				border-radius: 50rpx;
				margin: 0 auto;
				padding-top: 22rpx;
				padding-left: 30rpx;
				position: relative;
				// box-shadow: 5px 8px 8px rgba(0, 0, 0, 0.1);
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
		// 横线
		.hangxian{
			width: 100%;
			height: 1rpx;
			background-color: #ebebeb;
			margin-top: 20rpx;
		}
		// 列表
		.list{
			width: 100%;
			height: 1017rpx;
			background-color: antiquewhite;
			display: flex;
			// 列表左
			.list_zuo{
				width: 160rpx;
				height: 1017rpx;
				background-color: aqua;
				.list_zuo_wenzi{
					width: 100%;
					height: 96rpx;
					background-color: #f7f7f7;
					text-align: center;
					line-height: 96rpx;
				}
			}
			// 列表右
			.list_you{
				width: 590rpx;
				height: 1017rpx;
				background-color: #fff;
				padding-left: 35rpx;
				// 标题
				.biaoti{
					width: 100%;
					height: 96rpx;
					background-color: #fff;
					line-height: 96rpx;
				}
				// 列表内容盒子
				.list_you_list{
					width: 100%;
					height: 190rpx;
					background-color: #fff;
					margin-top: 25rpx;
					display: flex;
					// 列表左盒子图片和文字
					.list_you_list_wenzi{
						width: 85%;
						height: 190rpx;
						background-color: #fff;
						display: flex;
						// 图片
						.list_you_list_wenzi_tupian{
							width: 187rpx;
							height: 190rpx;
							background-color: #fff;
							image{
								width: 187rpx;
								height: 190rpx;
							}
						}
						// 文字
						.list_you_list_wenzi_wenzi{
							width: 100%;
							height: 190rpx;
							background-color: #fff;
							padding-left: 15rpx;
							display: flex;
							flex-direction:column;
							text{
								font-size: 35rpx;
								font-weight: 550;
								margin-top: 3rpx;
							}
						}
					}
					// 列表右盒子加减
					.list_you_list_jiajian{
						width: 15%;
						height: 190rpx;
						background-color: #fff;
						// 图片
						.list_you_list_jiajian_tupian{
							width: 55rpx;
							height: 55rpx;
							background-color: darkolivegreen;
							margin-top: 100rpx;
							margin-left: 20rpx;
							text-align: center;
							line-height: 50rpx;
							background-color: #fe6b55;
							border-radius: 50%;
							text{
								font-size: 55rpx;
								font-weight: 500;
								color: #fff;
							}
						}
					}
				}
			}
		}
		// 购物车
		.gwc{
			width: 100%;
			height: 100rpx;
			background-color: darkgreen;
			display: flex;
			// 购物车左
			.gwc_zuo{
				width: 60%;
				height: 100rpx;
				background-color: #fff;
				display: flex;
				// 图片
				.gwc_zuo_tupian{
					width: 126rpx;
					height: 80rpx;
					// background-color: #fe6b55;
					margin-top: 10rpx;
					margin-left: 40rpx;
					// 图片
					image{
						width: 100%;
						height: 100%;
					}
				}
				// 文字
				.gwc_zuo_wenzi{
					width: 100%;
					height: 100rpx;
					// background-color: darkmagenta;
					line-height: 100rpx;
					padding-left: 10rpx;
					text{
						font-weight: 550;
					}
				}
			}
			// 购物车右
			.wgc_you{
				width: 40%;
				height: 100rpx;
				background-color: #ff7355;
				text-align: center;
				line-height: 100rpx;
				text{
					font-weight: 550;
					color: #fff;
				}
			}
		}
	}
</style>
