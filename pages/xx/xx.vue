<template>
	<view>
		<view class="top"></view>
		<view class="bg"></view>
		<view class="content">
			<view class="d1">
				<image class="dao" @click="xdbwg()" src="https://s2.loli.net/2022/04/10/l1jWitwbIYPSFGM.png"></image>
				<p class="wenzi">小岛博物馆</p>
			</view>
			<view class="d2">
				<image class="dao" @click="ceshi()" src="https://s2.loli.net/2022/04/10/2d5BImuwxNiLDnU.png"></image>
				<p class="wenzi">测试岛</p>
			</view>
			<view class="d3">
				<image class="dao" @click="youxi()" src="https://s2.loli.net/2022/04/10/njN2CBDp8TMcyi4.png"></image>
				<p class="wenzi">游戏岛</p>
			</view>
			<view class="d4">
				<image class="dao" @click="xuexi()" src="https://s2.loli.net/2022/04/10/FYnP8tolv9TQEyC.png"></image>
				<p class="wenzi">学习岛</p>
			</view>
			<view class="d5">
				<image class="dao" @click="shequ()" src="https://s2.loli.net/2022/04/10/S2DWlqcNGLwIQeF.png"></image>
				<p class="wenzi">小岛社区</p>
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
			xdbwg(){
				uni.navigateTo({
					url:"../xdbwg/xdbwg"
				})
			},
			ceshi(){
				uni.navigateTo({
					url:"../nl/nl?num=1"
				})
			},
			youxi(){
				uni.navigateTo({
					url:"../nl/nl?num=2"
				})
			},
			xuexi(){
				uni.navigateTo({
					url:"../nl/nl?num=3"
				})
			},
			shequ(){
				uni.navigateTo({
					url:"../shequ/shequ"
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
			background-image: url(https://s2.loli.net/2022/04/10/bwJKW14tvefyR3Y.png);
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
		}
		.d1{
			position: absolute;
			width: 230rpx;
			height: 230rpx;
			left: 100rpx;
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
			left: 330rpx;
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
			top: 535rpx;
			display: flex;
			flex-direction: column;
			justify-content: center;
			align-items: center;
		}
		.d5{
			position: absolute;
			width: 230rpx;
			height: 230rpx;
			left: 430rpx;
			top: 135rpx;
			display: flex;
			flex-direction: column;
			justify-content: center;
			align-items: center;
		}
</style>
