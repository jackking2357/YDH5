<template>
	<view class="page" style="background-color: #000;">
		<image class="back" src="../../static/left.png" mode="" @click="back"></image>
		<image class="icons" src="../../static/icons.png"></image>
		<view class="title">
			雨点
		</view>
		<view class="btn1" @click="navto(1)">
			<image class="icon" src="../../static/anzhuo.png" mode=""></image>
			<view class="" style="margin-left: 30rpx;">
				Android下载
			</view>
		</view>
		<view class="btn2" @click="navto(2)">
			<view class="">
				使用h5网页打开
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
		onLoad() {
			
		},
		methods:{
			popdetail(){
				this.$refs.popup.open()
			},
			close(){
				this.$refs.popup.close()
			},
			back() {
				uni.navigateBack({
					delta: 1
				});
			},
			navto(index) {
				if(index==1){
					// 下载安卓app
					window.open('http://97.74.80.11:9000/test/yudianapp.apk')
				}else {
					//跳转h5链接
					window.open('http://yudianrobot.com/yudian-main/#')
				}
			}
		}
	}
</script>

<style lang="scss">
	.popup {
		width: 670rpx;
		background-color: rgba(0, 0, 0,0.9);
		color: #FFFFFF;
		padding: 40rpx 40rpx 40rpx 80rpx;
		box-sizing: border-box;
		border-radius: 40rpx;
		font-size: 28rpx;
		position: relative;
		& > view:nth-child(3){
			margin-top: 30rpx;
		}
		& > view:nth-child(4){
			margin-top: 30rpx;
		}
		& > view:nth-child(5){
			margin-top: 30rpx;
		}
		& > view:nth-child(6){
			margin-top: 30rpx;
		}
		& > view:nth-child(7){
			
		}
		& > view:nth-child(8){
			margin-top: 30rpx;
		}
		& > view:nth-child(9){
			position: absolute;
			left: 30rpx;
			top: 40rpx;
			width: 20rpx;
			height: 80rpx;
			background-color: #FEDA9B;
		}
		& > view:nth-child(10){
			position: absolute;
			right: 40rpx;
			top: 40rpx;
			color: #FFFFFF;
			font-size: 30rpx;
		}
	}
.page {
		width: 750rpx;
		height: 100vh;
		background-size: 100% 100%;
		position: fixed;
	}
	
	.back {
		width: 40rpx;
		height: 40rpx;
		position: fixed;
		top: 80rpx;
		left: 30rpx;
	}
	
	.icons {
		width: 278rpx;
		height: 278rpx;
		margin: 280rpx 236rpx 0;
	}
	
	.title {
		text-align: center;
		font-size: 52rpx;
		font-family: pingFangSC-ZC,sans-serif;
		margin: 32rpx 0 68rpx;
		font-weight: 500;
		color: #ECB26A;
		background: linear-gradient(180deg, #F5CB8A 0%, #DE9C53 100%);
		-webkit-background-clip: text;
		-webkit-text-fill-color: transparent;
	}
	
	.tip {
		font-size: 28rpx;
		font-family: PingFangSC-Medium, PingFang SC;
		font-weight: 500;
		color: #FFFFFF;
		text-align: center;
	}
	.tip2 {
		font-size: 28rpx;
		font-family: PingFangSC-Medium, PingFang SC;
		font-weight: 500;
		color: #dfdfdf;
		text-align: center;
	}
	
	.btn1 {
		/* width: 606rpx; */
		height: 50rpx;
		background: linear-gradient(180deg, #FEDA9B 0%, #E5AD73 100%);
		border-radius: 16rpx;
		margin: 200rpx 72rpx 28rpx;
		display: flex;
		font-size: 36rpx;
		font-family:  pingFangSC-QX,sans-serif;
		font-weight: 400;
		color: #252525;
		height: 100rpx;
		// padding: 26rpx 168rpx 20rpx 158rpx;
		align-items: center;
		justify-content: center;
		/* padding-top: 26rpx; */
	}
	.btn1s {
		/* width: 606rpx; */
		height: 50rpx;
		background: #D3D3D3;
		border-radius: 16rpx;
		margin: 200rpx 72rpx 28rpx;
		display: flex;
		font-size: 36rpx;
		font-family:  pingFangSC-QX,sans-serif;
		font-weight: 400;
		color:#A2A2A2;
		justify-content: space-between;
		padding: 26rpx 168rpx 20rpx 158rpx;
		/* padding-top: 26rpx; */
	}
	.btn2s {
		/* padding-top: 26rpx; */
		height: 54rpx;
		background: #D3D3D3;
		border-radius: 16rpx;
		height: 100rpx;
		margin: 28rpx 72rpx;
		display: flex;
		font-size: 36rpx;
		font-family:  pingFangSC-QX,sans-serif;
		font-weight: 400;
		color: #A2A2A2;
		justify-content: center;
		align-items: center;
		// padding: 22rpx 168rpx 20rpx 158rpx;
	}
	
	.icon {
		width: 52rpx;
		height: 52rpx;
	}
	
	.btn2 {
		/* width: 606rpx; */
		height: 100rpx;
		background: linear-gradient(180deg, #FEDA9B 0%, #E5AD73 100%);
		border-radius: 16rpx;
		margin: 28rpx 72rpx;
		display: flex;
		font-size: 36rpx;
		font-family:  pingFangSC-QX,sans-serif;
		font-weight: 400;
		color: #252525;
		justify-content: center;
		align-items: center;
		// padding: 22rpx 168rpx 20rpx 158rpx;
	}
	
</style>
