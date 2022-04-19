<template>
	<view>
		<view class="top"></view>
		<view class="bg"></view>
		<view class="content">
			<view class="d1">
				<image class="dao" @click="shui" src="https://s2.loli.net/2022/04/19/gerEIpuoKVs3nHW.png"></image>
				<p class="wenzi">小岛水吧</p>
			</view>
			<view class="d2">
				<image class="dao" @click="jia()" src="https://s2.loli.net/2022/04/19/1TEeawvmI2NFOG4.png"></image>
				<p class="wenzi">小岛加油站</p>
			</view>
			<view class="d3">
				<image class="dao" @click="chao()" src="https://s2.loli.net/2022/04/19/cohYJRFsDa28C7L.png"></image>
				<p class="wenzi">小岛超市</p>
			</view>
			<view class="d4">
				<image class="dao" @click="you()" src="https://s2.loli.net/2022/04/19/FviboLchV4rslw7.png"></image>
				<p class="wenzi">小岛邮箱</p>
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
			shui(){
				uni.navigateTo({
					url:"../shuiba/shuiba"
				})
			},
			jia(){
				uni.navigateTo({
					url:"../jiayouzhan/jiayouzhan"
				})
			},
			chao(){
				uni.navigateTo({
					url:"../chaoshi/chaoshi"
				})
			},
			you(){
				uni.navigateTo({
					url:"../youxiang/youxiang"
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
			background-image: url(https://s2.loli.net/2022/04/19/CJRhub2GdBmHwTP.jpg);
		}
		.content{
			position: fixed;
			top: 0;
			left: 0;
			width: 100%;
		}
		.dao{
			width: 200rpx;
			height: 200rpx;
		}
		.wenzi{
			text-align: center;
			font-weight: 400;
			font-size: 40rpx;
			font-family: '幼圆';
			color: #006600;
		}
		.d1{
			position: absolute;
			width: 230rpx;
			height: 230rpx;
			left: 90rpx;
			top: 255rpx;
			display: flex;
			flex-direction: column;
			justify-content: center;
			align-items: center;
		}
		.d2{
			position: absolute;
			width: 230rpx;
			height: 230rpx;
			left: 130rpx;
			top: 495rpx;
			display: flex;
			flex-direction: column;
			justify-content: center;
			align-items: center;
		}
		.d3{
			position: absolute;
			width: 230rpx;
			height: 230rpx;
			left: 380rpx;
			top: 325rpx;
			display: flex;
			flex-direction: column;
			justify-content: center;
			align-items: center;
		}
		.d4{
			position: absolute;
			width: 230rpx;
			height: 230rpx;
			left: 350rpx;
			top: 575rpx;
			display: flex;
			flex-direction: column;
			justify-content: center;
			align-items: center;
		}
</style>
