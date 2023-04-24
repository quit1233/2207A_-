<template>
	<view class="box">
		<!-- 搜索框 -->
		<view class="search_box">
				<view class="search">
						<input type="text" placeholder="请输入内容"/>
						<image src="../../static/ICON/3.png" mode=""></image>
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
.box{
	width: 100%;
	padding-top: 5rpx;
	// 搜索框盒子
	.search_box{
		width: 100%;
		height: 70rpx;
		// 搜索
		.search{
			width: 90%;
			height: 70rpx;
			border-radius: 50rpx;
			background-color: antiquewhite;
			margin: 0 auto;
			padding-top: 20rpx;
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
}
</style>
