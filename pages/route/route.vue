<template>
	<view class="box">
		<!-- 头部 -->
		<view class="toubu">
			<!-- 头部左 -->
			<view class="toubu_zuo">
				<image src="../../static/ICON/icon_cha.png" mode=""></image>
				<text>已有4个行程</text>
			</view>
			<!-- 头部右 -->
			<view class="toubu_you">
				<image src="../../static/ICON/77.png" mode=""></image>
				<text>历史</text>
			</view>
		</view>
		
		<!-- 列表 -->
		<view class="list_box" v-for="(val,key) in list" :key="'menu_'+key">
			<!-- 上盒子 -->
			<view class="list_box_shang">
				<view class="list_box_shang_wenzi">
					<image src="../../static/ICON/92.png" mode=""></image>
					<text style="margin-left: 15rpx;">05-09 11:40 周三名厨上门</text>
				</view>
				<view class="list_box_shang_wenzi">
					<image src="../../static/ICON/91.png" mode=""></image>
					<text style="margin-left: 15rpx;">涪城区长虹国际大道翡翠绿湾1栋2单元1802</text>
				</view>
			</view>
			<!-- 图片 -->
			<view class="list_tupian">
				<image src="../../static/ICON/goods4.png" mode=""></image>
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
					<view>
						<image src="../../static/ICON/93.png" mode=""></image>
						<text @click="dianhua">电话</text>
					</view>
					<view>
						<image src="../../static/ICON/16.png" mode=""></image>
						<text>服务</text>
					</view>
				</view>
			</view>
			<!-- 我的订单 -->
			<view class="dingdan">
				<text>我的订单</text>
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
			},
			dianhua(){
				uni.showModal({
					title: '王艺达',
					content: '0816-6600825',
					cancelText:'取消',
					confirmText:'拨打电话',
					success: function (res) {
						if (res.confirm) {
							console.log('用户点击确定');
							uni.makePhoneCall({
								phoneNumber: '0816-6600825' //仅为示例
							});
						} else if (res.cancel) {
							console.log('用户点击取消');
						}
					}
				});
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
		padding-bottom: 40rpx;
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
			height: 790rpx;
			background-color: #fff;
			border-radius: 20rpx;
			margin: 0 auto;
			margin-top: 20rpx;
			box-shadow: 2rpx 5rpx 5rpx 5rpx rgba(0, 0, 0, 0.1);
			// 上盒子
			.list_box_shang{
				width: 100%;
				height: 130rpx;
				// background-color: blanchedalmond;
				padding-top: 1rpx;
				
				.list_box_shang_wenzi{
					width: 100%;
					height: 38rpx;
					// background-color: chocolate;
					margin-top: 15rpx;
					// margin-left: 26rpx;
					padding-left: 26rpx;
					display: flex;
					align-items:center;
					image{
						width: 32rpx;
						height: 32rpx;
						
					}
				}
			}
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
					// flex-direction:column;
					// margin-right: 20rpx;
					 // align-items:center;
					 
					 view{
						 display: flex;
						 flex-direction:column;
						 margin-right: 35rpx;
						 image{
						 	width: 42rpx;
						 	height: 42rpx;
						 	margin: 0 auto;
						 	margin-top: 18rpx;
						 }
						 text{
						 	margin: 0 auto;
						 	color: burlywood;
						 	font-weight: 500;
						 }
					 }
					 
					 
					
				}
			}
			// 我的订单
			.dingdan{
				width: 95%;
				height: 80rpx;
				background-color: #fe6a54;
				margin: 0 auto;
				margin-top: 10rpx;
				border-radius: 10rpx;
				display: flex;
				text{
					margin: 0 auto;
					margin-top: 13rpx;
					font-size: 35rpx;
					font-weight: 550;
					color: #fff;
				}
			}
		}
	}
</style>
