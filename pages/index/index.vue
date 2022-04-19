<template>
	<view>
		<view class="top"></view>
		<view class="bg"></view>
		<view class="content">
			<view class="xx" @click="xuesheng()"><p>←学生这边走</p></view>
			<view class="jz" @click="jiazhang()"><p>家长这边走→</p></view>
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
		methods: {
			/*
			(1)uni.navigateTo(OBJECT) 保留当前页面，跳转到应用内的某个页面
			(2)uni.redirectTo(OBJECT) 关闭当前页面，跳转到应用内的某个页面
			(3)uni.reLaunch(OBJECT) 关闭所有页面，打开到应用内的某个页面
			(4)uni.switchTab(OBJECT) 跳转到 tabBar 页面，并关闭其他所有非 tabBar 页面
			(5)uni.navigateBack(OBJECT) 关闭当前页面，返回上一页面或多级页面
			*/
		   xuesheng(){
			   uni.redirectTo({
			   	url:"../xx/xx"
			   })
		   },
		   jiazhang(){
			   uni.redirectTo({
			   	url:"../jz/jz?num"
			   })
		   }
		}
	}
</script>

<style>
	.top {
			height: var(--status-bar-height);
			width: 100%;
			background-color: #FFFFFF;
		}
	.bg{
			position: fixed;
			top: 0;
			left: 0;
			width: 100%;
			height: 100%;
			z-index: -10;
			background-repeat: no-repeat;
			background-size: 100% 100%;
			background-image: url(https://s2.loli.net/2022/04/19/FzIkP2clOdmU5Tw.jpg);
		}
		.content{
			position: fixed;
			top: 0;
			left: 0;
			width: 100%;
		}
		.ym{
			display: block;
			width: 430rpx;
			height: 200rpx;
			margin: 0 auto;
			margin-top: 200rpx;
		}
		.xx{
			width: 450rpx;
			height: 90rpx;
			background: yellow;
			border-radius: 35rpx;
			border: #F0AD4E solid 5rpx;
			margin: 0 auto;
			display: flex;
			flex-direction: row;
			justify-content: center;
			align-items: center;
			margin-top: 400rpx;
			font-weight: 600;
		}
		.jz{
			width: 450rpx;
			height: 90rpx;
			background: yellow;
			border-radius: 35rpx;
			border: #2C405A solid 5rpx;
			margin: 0 auto;
			display: flex;
			flex-direction: row;
			justify-content: center;
			align-items: center;
			margin-top: 50rpx;
			font-weight: 600;
		}
		.wz{
			isplay: flex;
			flex-direction: row;
			justify-content: center;
			align-items: center;
			margin-top: 50rpx;
		}
		.p1,.p2,.p3,.p4{
			margin-top: 30rpx;
			text-align: center;
			color: #333333;
		}
</style>
