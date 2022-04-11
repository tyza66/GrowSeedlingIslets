<template>
	<view>
		<view class="top"></view>
		<view class="bg"></view>
		<view class="xx"><p>小岛社区</p></view>
		<view class="items">
					<view class="item">
						<image src="https://s2.loli.net/2022/04/11/BM7bCiU1SzjxOZR.png"></image>
						<p>雷军</p>
					</view>
					<view class="item">
						<image src="https://s2.loli.net/2022/04/11/rvw2PuQNxLdGBhc.png"></image>
						<p>王健林</p>
					</view>
					<view class="item">
						<image src="https://s2.loli.net/2022/04/11/BVJTz5svNrinKgj.png"></image>
						<p>马云</p>
					</view>
		</view>
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
						["https://s2.loli.net/2022/04/11/zp7QEqXHgLFho2A.png","羙锝凄凉","学习是一件因人而异的东西，有些人觉得很简单，而有些人却觉得很难。其实学习既要方法，也要学习者的恒心、毅力。"],
						["https://s2.loli.net/2022/04/11/XFoSPxeE2Na91Cb.png","故事猜不透.","学习语文至关重要，因为它是我们语言的基础，学会了它才能与人进行交流。我们必须学好课本上的知识，加强习作训练；还要广泛阅读课外书物，积累好词好句并把它运用到实际行动中。"],
						["https://s2.loli.net/2022/04/11/G7woWaiFCU3fKZO.png","嘉言","学习数学一是学习态度得好，还得有好学习方法；我们首先得在书中阶段培养数学运算能力。算题时要情绪稳定，看清楚再下笔，尽量做到一便成功；学数学没有捷径可走，保证做题的数量和质量是学好数学的必经之路。"],
						["https://s2.loli.net/2022/04/11/eCBxJMP9g2hcYFf.png","永追随向日葵","学英语，首先要培养对英语的兴趣。“兴趣是最好的老师”，兴趣是学习英语的巨大动力，有了兴趣，学习就会事半功倍。很多人认为背单词难，而我的经验就是口中大声的读，用笔在纸上写。做到这些背单词就很简单了。"],
						["https://s2.loli.net/2022/04/11/jFz7TV8hAUn2JWc.png","芙蓉姐姐","在别人不督促的情况下，要能主动学习，而且一学习就要求自己立刻进入状态，投入其中，不要在学习的同时干其他事或想其他事，比如边学习边听音乐，这段时间听音乐不能放松神经，只会适得其反。如果能长久地专心于学习，成绩定会提高。"],
						["https://s2.loli.net/2022/04/11/pfw4UA8RmCKq6rO.png","执着是爱的痛","对于老师布置的任务，要即时完成，这一点很重要，它相当于一个基本的学习起点，切忌似懂非懂，而且对于订正不能得过且过，必须充分理解，最好再做一遍。"],
						["https://s2.loli.net/2022/04/11/kNVaQufh1Kq46jv.png","多一度旳想念","在专心听讲的同时，要动笔做简单记录或记号。这样做既方便自己复习，也可以记住更多要点。但有时一节课不需要都去记笔记，更多的是需要理解、吸收老师讲的内容。"],
						["https://s2.loli.net/2022/04/11/lyt9LNrOBk5U12f.png","太现实的现实","在背诵方面，也是一样，不能死记硬背，最好是在对诗词、古文有了一定了解的基础上进行背诵，这样不仅不容易忘记，还不会出错。"],
						["https://s2.loli.net/2022/04/11/4ToGxPurCBSYqw5.png","始情．","说起经验，什麽是经验呢？经验就是从多次实践中得到的知识或技能，但对学习来说就是在失败中找成功，从成功中找进步。"]
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
		background: url(https://s2.loli.net/2022/04/11/8gq4HKGcUDnh1uJ.png);
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
	.items{
			width: 100%;
			height: 180rpx;
			display: flex;
			flex-direction: row;
			justify-content: center;
			align-items: center;
		}
		.item{
			width: 180rpx;
			height: 180rpx;
			margin: 0 auto;
			display: flex;
			flex-direction: column;
			justify-content: center;
			align-items: center;
		}
		.item image{
			width: 100rpx;
			height: 100rpx;
		}
</style>