<template>
	<view class="box">
		<!-- 头部 -->
		<view class="toubu">
			<!-- 头部左 -->
			<view class="toubu_zuo">
				<image src="../../static/ICON/icon_cha.png" mode=""></image>
				<text>收藏12个餐宴</text>
			</view>
			<!-- 头部右 -->
			<view class="toubu_you">
				<image src="../../static/ICON/icon_clear.png" mode=""></image>
				<text>清空</text>
			</view>
		</view>
		<!-- 列表 -->
		<view class="list_box" v-for="(val,key) in list" :key="'menu_'+key">
			<!-- 图片 -->
			<view class="list_tupian">
				<image :src="val.pic" mode=""></image>
			</view>
			<!-- 文字 -->
			<view class="list_wenzi">
				<!-- 文字左盒子 -->
				<view class="list_wenzi_zuo">
					<text>{{val.goodsname}}</text>
					<text style="color: brown;">￥{{val.price}}/桌</text>
				</view>
				<!-- 文字右盒子 -->
				<view class="list_wenzi_you">
					<image src="../../static/ICON/footer2.png" mode=""></image>
					<text>取消收藏</text>
				</view>
			</view>
		</view>

	</view>
</template>

<script>
	export default {
		data() {
			return {
				list:[]
			}
		},
		created(){
			this.getList()
		},
		methods: {
			getList(){
				uni.request({
					url:'http://api.brqc.com.cn/cpz/shxmp/goodslist',
					data:{},
					success:(res)=>{
						console.log(res.data);
						this.list = res.data.data
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
	.box{
		width: 100%;
		padding-bottom: 30rpx;
		// 头部
		.toubu{
			width: 96%;
			height: 90rpx;
			background-color: #fff;
			margin: 0 auto;
			display:flex;
			justify-content:space-between;
			// 头部左
			.toubu_zuo{
				width: 84%;
				height: 90rpx;
				// background-color: blanchedalmond;
				display: flex;
				align-items: center;
				image{
					width: 40rpx;
					height: 40rpx;
				}
				text{
					margin-left: 10rpx;
					font-size: 35rpx;
					font-weight: 550;
					color: #333;
				}
			}
			// 头部右
			.toubu_you{
				width: 16%;
				height: 90rpx;
				// background-color: brown;
				display: flex;
				// flex-direction:column-reverse;
				align-items: center;
				image{
					width: 40rpx;
					height: 40rpx;
				}
				text{
					margin-left: 10rpx;
					font-weight: 550;
					color: #999;
				}
			}
		}
		// 列表盒子
		.list_box{
			width: 96%;
			height: 549rpx;
			background-color: #fff;
			border-radius: 20rpx;
			margin: 0 auto;
			margin-top: 20rpx;
			box-shadow: 2px 3px 3px rgba(0, 0, 0, 0.1);
			// 图片
			.list_tupian{
				width: 100%;
				height: 424rpx;
				// background-color: blue;
				image{
					width: 100%;
					height: 100%;
					border-radius: 20rpx;
				}
			}
			// 文字
			.list_wenzi{
				width: 100%;
				height: 125rpx;
				// background-color: aqua;
				display: flex;
				justify-content: space-between;
				// 文字左盒子
				.list_wenzi_zuo{
					// width: 50%;
					height: 125rpx;
					// background-color: cadetblue;
					display: flex;
					flex-direction:column;
					margin-left: 20rpx;
					// padding-top: 18rpx;
					text{
						font-size: 34rpx;
						font-weight: 600;
						margin-top: 10rpx;
						
					}
					
				}
					
				.list_wenzi_you{
					// width: 50%;
					height: 125rpx;
					// background-color: chartreuse;
					display: flex;
					flex-direction:column;
					margin-right: 20rpx;
					 // align-items:center;
					image{
						width: 42rpx;
						height: 42rpx;
						margin: 0 auto;
						margin-top: 18rpx;
					}
					text{
						margin: 0 auto;
						color: #666;
						font-weight: 500;
					}
				}
			}
		}
	}
	
	
</style>
