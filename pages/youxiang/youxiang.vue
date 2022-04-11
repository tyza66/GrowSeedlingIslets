<template>
	<view>
		<view class="top"></view>
		<view class="bg"></view>
		<view class="dongtai" v-for="(item,i) in dt">
			<view class="user"><image :src="item[0]"><p>{{item[1]}}</p></view>
			<view class="xiaoxi">{{item[2]}}</view>
		</view>
	</view>
</template>

<script>
	export default {
		data() {
			return {
				xian: false,
				out:"",
					dt:[
						["https://s2.loli.net/2022/04/11/OrEQdV4ihDjxz59.png","一语呢喃","这个平台真的太好了，帮助很大！"],
						["https://s2.loli.net/2022/04/11/sPAoIRHQKzgUFjh.png","南馆潇湘.","我儿子的学习成绩突飞猛进！赞！"],
						["https://s2.loli.net/2022/04/11/ViomSUzZfNIEjFx.png","闺怨无梦","我觉得学习笑道的功能可以更多的拓展一下"],
						["https://s2.loli.net/2022/04/11/eCBxJMP9g2hcYFf.png","被冲淡的悲伤","有一个bug希望团队早日解决"],
						["https://s2.loli.net/2022/04/11/HXlTVyvMgYNbCPw.png","花开一夜","希望你们做的越来越好！"],
					]
				}
		},
		methods: {
			
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
		background-image: url(https://s2.loli.net/2022/04/11/z5CPqEbVns41HAr.png);
		background-repeat: no-repeat;
		background-size: 100% 100%;
	}
	.xx{
		width: 100%;
		height: 60rpx;
		display: flex;
		flex-direction: row;
		justify-content: center;
		align-items: center;
	}
	.xx p{
		font-size: 45rpx;
		color: #FFFFFF;
	}
	.dongtai{
		width: 100%;
	}
	.dongtai .user{
		height: 100rpx;
		display: flex;
		flex-direction: row;
		justify-content: left;
		align-items: cneter;
	}
	.dongtai .user image{
		width: 100rpx;
		height: 100rpx;
		border-radius: 50rpx;
		margin-left: 30rpx;
	}
	.dongtai .user p{
		font-size: 60rpx;
		height: 30rpx;
		margin-top: 10rpx;
	}
	.xiaoxi{
		width: 80%;
		margin: 0 auto;
	}
	.jia{
		position: fixed;
		z-index: 1000;
		right: 10rpx;
		top: 1100rpx;
		width: 100rpx;
		height: 100rpx;
		border-radius: 50rpx;
		background: #FFD700;
		display: flex;
		flex-direction: column;
		justify-content: center;
		align-items: cneter;
	}
	.jia p{
		margin: 0 auto;
		margin-top: -40rpx;
		width: 50rpx;
		height: 50rpx;
		font-size: 60rpx;
		text-align: center;
	}
	.shi{
		position: fixed;
		z-index: 500;
		left: 25rpx;
		top: 700rpx;
		width: 700rpx;
		height: 300rpx;
		border-radius: 30rpx;
		background: #FFD700;
		display: flex;
		flex-direction: column;
		justify-content: center;
		align-items: cneter;
	}
	.shuru{
		width: 600rpx;
		height:	300rpx;
		margin: 0 auto;
		margin-top: 50rpx;
		background: #C8C7CC;
	}
	.shuru textarea{
		width: 100%;
		height: 100%;
	}
	.tijiao{
		width: 140rpx;
		margin: 0 auto;
		text-align: center;
		background: red;
		border: #000000 solid 1px;
		border-radius: 5rpx;
	}
	
</style>