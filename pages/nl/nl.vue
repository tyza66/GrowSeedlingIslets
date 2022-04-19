<template>
	<view>
		<view class="top"></view>
		<view class="bg"></view>
		<view class="content">
			<p class="m">选择你的年龄段：</p>
			<view class="ys" @click="ys1()"><p>1-3年级</p></view>
			<view class="sl" @click="sl1()"><p>4-6年级</p></view>
		</view>
	</view>
</template>

<script>
	export default {
		onLoad(option) {
			console.log(option.num);
			this.way = parseInt(option.num);
		},
		data() {
			return {
				way: 1
			}
		},
		methods: {
			ys1(){
				switch(this.way){
					case 1: uni.redirectTo({
						url:"../ceshi/ceshi"
					});break;
					case 2: uni.redirectTo({
						url:"../youxidao/youxidao"
					});break;
					case 3: uni.redirectTo({
						url:"../xuexi/xuexi"
					});break;
				}
			},
			sl1(){
				switch(this.way){
					case 1: uni.redirectTo({
						url:"../ceshi/ceshi"
					});break;
					case 2: uni.redirectTo({
						url:"../youxidao/youxidao"
					});break;
					case 3: uni.redirectTo({
						url:"../xuexi/xuexi"
					});break;
				}
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
		.m{
			text-align: center;
			font-size: 55rpx;
			margin-top: 300rpx;
		}
		.ys{
			width: 450rpx;
			height: 90rpx;
			background: gold;
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
		.sl{
			width: 450rpx;
			height: 90rpx;
			background: gold;
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
</style>
