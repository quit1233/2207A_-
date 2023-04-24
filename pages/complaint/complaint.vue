<template>
	<view class="box">
		<!-- 投诉类型 -->
		<view class="leixing">
			<!-- 文字 -->
			<view class="wenzi">
				投诉类型
			</view>
			<!-- 详情 -->
			<view class="xiangqing">
				<view style="background-color: #fc6b53;">
					<text>服务态度</text>
				</view>
				<view>
					<text>服务态度</text>
				</view>
				<view>
					<text>服务态度</text>
				</view>
			</view>
		</view>
		<!-- 反馈 -->
		<view class="fankui">
			<!-- 文本框 -->
			<view class="wenben">
				<textarea name="comments" placeholder="输入投诉详细说明(选填)"></textarea>
			</view>
			<!-- 上传图片 -->
			<view class="tupian">
				<view class="shangchuan">
					<text>+</text>
				</view>
			</view>
		</view>
		<!-- 提交 -->
		<view class="tijiao">
			<text>提交</text>
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
		// 投诉类型
		.leixing{
			width: 96%;
			height: 177rpx;
			// background-color: aqua;
			margin: 0 auto;
			padding-top: 20rpx;
			border-bottom: 1rpx solid #999;
			// 文字
			.wenzi{
				width: 100%;
				height: 45rpx;
				// background-color: antiquewhite;
				font-weight: 800;
			}
			// 详情
			.xiangqing{
				width: 100%;
				height: 55rpx;
				// background-color: chartreuse;
				margin-top: 25rpx;
				display: flex;
				
				view{
					width: 165rpx;
					height: 55rpx;
					background-color: #fff;
					text-align:center;
					line-height: 55rpx;
					border-radius: 28rpx;
					border: 1rpx solid #999;
					// margin-top: 10rpx;
					margin-left: 15rpx;
				}
				
				
			}
		}
		// 反馈
		.fankui{
			width: 96%;
			// height: 470rpx;
			margin: 0 auto;
			// background-color: chartreuse;
			// 文本框
			.wenben{
				width: 100%;
				height: 300rpx;
				// background-color: chocolate;
				padding-top: 15rpx;
			}
			// 上传图片
			.tupian{
				width: 100%;
				height: 616rpx;
				// background-color: cornflowerblue;
				.shangchuan{
					width: 160rpx;
					height: 160rpx;
					background-color: #f3f3f3;
					text-align: center;
					line-height: 160rpx;
					
					text{
						font-size: 100rpx;
						color: #999;
					}
				}
			}
		}
		// 提交
		.tijiao{
			width: 100%;
			height: 100rpx;
			background-color: coral;
			text-align: center;
			line-height: 100rpx;
			font-size: 38rpx;
			color: #fff;
			margin-top: 53rpx;
		}
		
	}
</style>
