<template>
	<view class="box">
		<!-- 头部 -->
		<view class="toubu">
			<!-- 头部左 -->
			<view class="toubu_zuo">
				<text style="font-weight: 550;">天下第壹吃货</text>
				<text>欢迎您光临四海香!</text>
			</view>
			<!-- 头部右 -->
			<view class="toubu_you">
				<image src="../../static/ICON/man2.jpg" mode=""></image>
			</view>
		</view>
		<!-- 列表 -->
		<view class="list">
			<!-- 列表左 -->
			<view class="list_zuo">
				<image src="../../static/ICON/icon_order.png" mode=""></image>
				<text>烹饪历史</text>
			</view>
			<!-- 列表右 -->
			<view class="list_you">
				<text>></text>
			</view>
		</view>
		<!-- 列表 -->
		<view class="list">
			<!-- 列表左 -->
			<view class="list_zuo">
				<image src="../../static/ICON/icon_money.png" mode=""></image>
				<text>支付记录</text>
			</view>
			<!-- 列表右 -->
			<view class="list_you">
				<text>></text>
			</view>
		</view>
		<!-- 列表 -->
		<view class="list">
			<!-- 列表左 -->
			<view class="list_zuo">
				<image src="../../static/ICON/icon_msg.png" mode=""></image>
				<text>举报投诉</text>
			</view>
			<!-- 列表右 -->
			<view class="list_you">
				<navigator url="/pages/complaint/complaint"><text>></text></navigator>
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
		// 头部
		.toubu{
			width: 100%;
			height: 210rpx;
			// background-color: antiquewhite;
			border-bottom: 1rpx solid #eee;
			display: flex;
			justify-content:space-between;
			align-items:center;
			// 头部左
			.toubu_zuo{
				height: 132rpx;
				// background-color: aqua;
				display: flex;
				flex-direction:column;
				margin-left: 4%;
				text{
					font-size: 35rpx;
					margin-top: 10rpx;
				}
			}
			// 头部右
			.toubu_you{
				height: 132rpx;
				// background-color: beige;
				border-radius: 50%;
				margin-right: 4%;
				image{
					width: 132rpx;
					height: 132rpx;
					border-radius: 50%;
				}
			}
			
		}
		// 列表盒子
		.list{
			width: 100%;
			height: 95rpx;
			// background-color: chartreuse;
			border-bottom: 1rpx solid #eee;
			display: flex;
			justify-content:space-between;
			align-items:center;
			// 列表左盒子
			.list_zuo{
				height: 44rpx;
				// background-color: darkblue;
				display: flex;
				margin-left: 4%;
				image{
					width: 44rpx;
					height: 44rpx;
				}
				text{
					font-size: 35rpx;
					margin-left: 20rpx;
					font-weight: 500;
				}
			}
			// 列表右盒子
			.list_you{
				// height: 44rpx;
				// background-color: darkcyan;
				display: flex;
				margin-right: 4%;
				text{
					font-size: 45rpx;
					font-weight: 800;
					margin: 0 auto;
				}
			}
		}
	}
</style>
