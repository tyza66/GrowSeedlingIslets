<template>
	<view class="index">
		<view class="new_box" style="margin-top: 20upx;">
			<view class="bbox">
				<view class="list-box" v-for="(item,index) in list" :key="index">
					<view class="list-ed">
						<image class="list-img" :src="item.src" mode="aspectFill"></image>
						<view class="list-right">
							<view class="list-head" @click="choice(index)">
								<view :class="[item.selected?'selde':'noselde']">{{item.selected?"已收藏":"未收藏"}}<text :class="[item.selected?'selde-q':'noselde-q']"></text></view>
							</view>
							<view class="list-name">{{item.title}}</view>
							<view class="list-da">
								<view>简介：<text>{{item.course}}</text></view>
 
							</view>
						</view>
					</view>
				</view>
			</view>
		</view>
	</view>
</template>
 
<script>
	export default {
		data() {
			return {
				list: [{
						course_id: "001",
						title: "生涯教育（图文）",
						course: "生涯教育起源于日本...",
						selected: true,
						src : "https://s2.loli.net/2022/04/10/9tFyvio7MwLDGrB.jpg"
					},
					{
						course_id: "002",
						title: "生涯教育（视频）",
						course: "每节课一分钟,拓展眼界...",
						selected: true,
						src:"https://s2.loli.net/2022/04/10/Aylr6Z7H4PERVx5.png"
					},
					{
						course_id: "003",
						title: "小而优”学校本土化特色工匠",
						course: "学校本土化特色工做课程",
						selected: false,
						src:"https://s2.loli.net/2022/04/10/ht9gfNSvFnm4AJu.png"
					},
 
					{
						course_id: "004",
						title: "特色小课程(图文)",
						course: "神奇特色小课程",
						selected: false,
						src:"https://s2.loli.net/2022/04/10/C27mYiZNMR9HTpU.jpg"
					},
					{
						course_id: "005",
						title: "超舒适学习背景视频",
						course: "数据科学与大数据技术",
						selected: false,
						src:"https://s2.loli.net/2022/04/10/vr9tCXuV41dqBH3.png"
					},
					{
						course_id: "006",
						title: "2021学习视频合集",
						course: "陪伴学习",
						selected: false,
						src:"https://s2.loli.net/2022/04/10/yvFqSuG4VL3O5lB.png"
					},
					{
						course_id: "007",
						title: "一步步攀登",
						course: "新时代学习理念",
						selected: false,
						src:"https://s2.loli.net/2022/04/10/xFkQLOAWVhzBtp8.png"
					}
				],
				selectId:[],
			};
		},
		methods: {
			//选择课程
			choice(index){
				if(this.list[index].selected == true){
					this.list[index].selected = false;
					//取消选中时删除数组中的值
					for(var i = 0; i < this.selectId.length; i++){
					    if(this.selectId[i] === this.list[index].course_id){
					        this.selectId.splice(i,1);
					    }
					}
					console.log("选中的值",this.selectId)
				}else{
					this.list[index].selected = true;
					this.selectId.push(this.list[index].course_id)
					console.log("选中的值",this.selectId)
				}
			},
		
		}
	};
</script>
 
<style>
	page{
		background-color: #eee;
	}
	/* 已选择 */
	.selde {
		border: 1px solid black;
		background: black;
		color: #f0f0f0;
		border-radius: 20upx;
		display: flex;
		flex-direction: row;
		justify-content: center;
		align-items: center;
		font-size: 20upx;
		padding: 0 10upx;
	}
 
	.selde-q {
		
		width: 18upx;
		height: 18upx;
		border-radius: 50%;
		background: #ffffff;
		margin-left: 6upx;
	}
 
	/* 未选择 */
	.noselde {
		
		border: 1px solid #959595;
		background: #FFFFFF;
		color: #959595;
		border-radius: 20upx;
		display: flex;
		flex-direction: row;
		justify-content: center;
		align-items: center;
		font-size: 20upx;
		padding: 0 10upx;
	}
 
	.noselde-q {
		
		border: 1px solid #959595;
		width: 16upx;
		height: 16upx;
		border-radius: 50%;
		background: #FFFFFF;
		margin-left: 6upx;
	}
	.list-box {
		
		display: flex;
		flex-direction: column;
		background-color: #fff;
		margin: 0upx 16upx 16upx 16upx;
		padding: 16upx;
		border-radius: 10upx;
	}
 
	.list-ed {
		font-size: 40rpx;
		display: flex;
		flex-direction: row;
		justify-content: center;
		align-items: center;
	}
 
	.list-left {
		margin-right: 16upx;
	}
 
	.list-img {
		
		width: 160upx;
		height: 160upx;
		margin: 0upx 16upx 0upx 0upx;
	}
 
	.list-right {
		
		display: flex;
		flex-direction: column;
		width: 510upx;
		height: 180upx;
	}
 
	.list-right-img {
		width: 140upx;
		height: 38upx;
	}
 
	.noadsop {
		width: 120upx;
		height: 32upx;
	}
 
	.list-head {
		
		display: flex;
		justify-content: flex-end;
		margin-bottom: 10upx;
	}
 
	.list-name {
		overflow: hidden;
		text-overflow: ellipsis;
		display: -webkit-box;
		-webkit-box-orient: vertical;
		-webkit-line-clamp: 2;
		margin-bottom: 10upx;
	}
 
	.list-da {
		
		display: flex;
		flex-direction: row;
		font-size: 26upx;
	}
 
	.list-da view {
		
		width: 50%;
	}
 
	.list-da view text {
		
		color: f0f0f0;
	}
 
	.sure {
		
		background: #FF6000;
		color: #FFFFFF;
		width: 600upx;
		height: 70upx;
		display: flex;
		justify-content: center;
		align-items: center;
		border-radius: 40upx;
		margin: 60upx auto;
	}
</style>