<template>
	<view>
		<view class="top"></view>
		<view class="bg"></view>
		<view class="xx"><p>小岛水吧</p></view>
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
						["https://s2.loli.net/2022/04/11/KoiURZPzdAhp1cG.png","魔法唧唧","父母是子女在生活中一切言行举止的最早启蒙老师。"],
						["https://s2.loli.net/2022/04/11/m1pKWhR35zZXrTn.png","猜不透","天赋如同自然花木，要用来修剪。"],
						["https://s2.loli.net/2022/04/11/eh6FJSCKvjmwrgp.png","轻烟薄雾","孩子在幼儿期间，蕴藏着无限的可能性，需要父母加以挖掘和引导。"],
						["https://s2.loli.net/2022/04/11/eCBxJMP9g2hcYFf.png","永追随向日葵","一个人的成功=1%IQ—智商+99%EQ—情商。"],
						["https://s2.loli.net/2022/04/11/eh6FJSCKvjmwrgp.png","芙蓉姐姐","父母是孩子认识世界获取知识的第一所学校。"],
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
		background-image: url(https://s2.loli.net/2022/04/11/tRmzGC8eONoSuy9.png);
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