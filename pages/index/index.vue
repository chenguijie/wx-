<template>
	<view>
		<swiper :indicator-dots="true" indicator-active-color="#999" indicator-color="#333" :autoplay="true">
			<!-- 轮播图 -->
			<swiper-item>
				<image style="width:100%;height:350rpx;flex-shrink: 0;" src="https://bkimg.cdn.bcebos.com/pic/6609c93d70cf3bc73297f48cd600baa1cd112a3e?x-bce-process=image/resize,m_lfit,w_500,h_500,limit_1"  ></image>
			</swiper-item>
			<swiper-item>
				<image src="https://bkimg.cdn.bcebos.com/pic/11385343fbf2b211c29cbc2ecd8065380cd78e1b?x-bce-process=image/resize,m_lfit,w_500,h_500,limit_1" style="width: 100%;height: 350rpx;flex-shrink: 0;"></image>
			</swiper-item>
			<swiper-item>
				<image src="https://imgsrc.baidu.com/baike/pic/item/a50f4bfbfbedab646bf7068ff936afc378311ef3.jpg" style="flex-shrink: 0;width: 100%;"></image>
			</swiper-item>
		</swiper>
		<view>
			<!-- 分割线 -->
			<rich-text :nodes="nodedata"></rich-text>
			<view class="divLine"></view>
		</view>
		<view class="con1">
			<view class="text1">人物介绍</view>
			<view class="im1">
				
				<view class="v1" v-for="data in viewdata1" :key="data.id">
					<view @click="dataClick(data)">
						<view class="vnv1">
							<image :src="data.imgsrc" style="width: 100%" mode="widthFix"></image>
						</view>
						<text>{{data.name}}</text>
					</view>
				</view>
				
			</view>
		</view>
	</view>
</template>

<script>
	export default {
		data(){
			return{
				nodedata:'<h1 style="color:aqua;text-align:center">偶像大师</h1>',
				viewdata1:[
					{id:1,name:'天海春香',imgsrc:'https://ss1.bdstatic.com/70cFvXSh_Q1YnxGkpoWK1HF6hhy/it/u=4205093878,3227470771&fm=26&gp=0.jpg'},
					{id:2,name:'星井美希',imgsrc:'https://ss1.bdstatic.com/70cFvXSh_Q1YnxGkpoWK1HF6hhy/it/u=23248051,102316236&fm=26&gp=0.jpg'},
					{id:3,name:'如月千早',imgsrc:"https://ss2.bdstatic.com/70cFvnSh_Q1YnxGkpoWK1HF6hhy/it/u=1980642055,1482418531&fm=26&gp=0.jpg"},
					{id:4,name:'高槻弥生',imgsrc:"https://ss0.bdstatic.com/70cFuHSh_Q1YnxGkpoWK1HF6hhy/it/u=3913834368,3742267568&fm=26&gp=0.jpg"},
					{id:5,name:'萩原雪步',imgsrc:"https://ss1.bdstatic.com/70cFvXSh_Q1YnxGkpoWK1HF6hhy/it/u=1643020123,3218348056&fm=26&gp=0.jpg"},
					{id:6,name:'菊地真',imgsrc:"https://ss1.bdstatic.com/70cFvXSh_Q1YnxGkpoWK1HF6hhy/it/u=223020402,2830240075&fm=26&gp=0.jpg"},
					{id:7,name:'双海亚美',imgsrc:"https://ss1.bdstatic.com/70cFuXSh_Q1YnxGkpoWK1HF6hhy/it/u=1041027040,3495264605&fm=26&gp=0.jpg"},
					{id:8,name:'双海真美',imgsrc:"https://ss1.bdstatic.com/70cFvXSh_Q1YnxGkpoWK1HF6hhy/it/u=3035712070,401862567&fm=26&gp=0.jpg"},
					{id:9,name:'水瀬伊织',imgsrc:"https://ss1.bdstatic.com/70cFvXSh_Q1YnxGkpoWK1HF6hhy/it/u=3533369924,4207282107&fm=15&gp=0.jpg"},
					{id:10,name:'三浦梓',imgsrc:"https://ss1.bdstatic.com/70cFuXSh_Q1YnxGkpoWK1HF6hhy/it/u=1427728969,2602776472&fm=15&gp=0.jpg"},
					{id:11,name:'四条贵音',imgsrc:"https://ss3.bdstatic.com/70cFv8Sh_Q1YnxGkpoWK1HF6hhy/it/u=3784340444,4965487&fm=26&gp=0.jpg"},
					{id:12,name:'我那霸响',imgsrc:"https://ss0.bdstatic.com/70cFvHSh_Q1YnxGkpoWK1HF6hhy/it/u=3290565215,1443289031&fm=26&gp=0.jpg"},
					{id:13,name:'秋月律子',imgsrc:"https://ss1.bdstatic.com/70cFuXSh_Q1YnxGkpoWK1HF6hhy/it/u=4241572781,3290307196&fm=26&gp=0.jpg"},
					{id:14,name:'音无小鸟',imgsrc:"https://ss0.bdstatic.com/70cFuHSh_Q1YnxGkpoWK1HF6hhy/it/u=3292049286,259799734&fm=15&gp=0.jpg"}
				]
			}
		},
		methods: {
			dataClick(data){
				var newData=JSON.stringify(data)
				
				uni.navigateTo({
					url:'./Introduction?index='+encodeURIComponent( newData)
				})
				
			}
		}
	}
</script>

<style lang="less">
	*{
		margin-top: 10rpx;
	}
	.divLine{
		width: 750rpx;
		height: 15rpx;
		border-bottom: 5rpx solid #999;
	}
	.con1{
		margin: 10rpx;
		.text1{
			text-align: center;
			font-family: 华文隶书;
		}
		.im1{
			text-align: center;
			.v1{
				width: 220rpx;
				height: 325rpx;
				background-color: #999;
				margin: 10rpx;
				overflow: hidden;
				float: left;text-align: center;
				.vnv1{
					height: 275rpx;
				}
				text{
					font-family: 华文新魏;
					color: aqua;
				}
			}
		}
	}
	
</style>
