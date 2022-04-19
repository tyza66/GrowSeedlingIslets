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
			width: 300rpx;
			height: 300rpx;
		}
		.wenzi{
			text-align: center;
			font-weight: 600;
			font-size: 30rpx;
			color: #006600;
			margin-top: -15rpx;
		}
		.d1{
			position: absolute;
			width: 300rpx;
			height: 330rpx;
			left: 30rpx;
			top: 225rpx;
			display: flex;
			flex-direction: column;
			justify-content: center;
			align-items: center;
		}
		.d2{
			position: absolute;
			width: 300rpx;
			height: 330rpx;
			left: 100rpx;
			top: 605rpx;
			display: flex;
			flex-direction: column;
			justify-content: center;
			align-items: center;
		}
		.d3{
			position: absolute;
			width: 300rpx;
			height: 330rpx;
			left: 350rpx;
			top: 305rpx;
			display: flex;
			flex-direction: column;
			justify-content: center;
			align-items: center;
		}
		.d4{
			position: absolute;
			width: 300rpx;
			height: 330rpx;
			left: 380rpx;
			top: 675rpx;
			display: flex;
			flex-direction: column;
			justify-content: center;
			align-items: center;
		}
</style>
