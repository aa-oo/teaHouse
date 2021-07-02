<template>
	<view>
		<!-- 名该片 -->
		<view class="buscardTop">
			<div class="hm-friend-information-card">
				<view class="box2" style="margin-top: 45rpx;position: relative">
					<view class="buscardright"><image class="buscardImg" :src="productList[1].image_src" />
						<!-- <view v-if="collected" class="collectcard" >已收藏</view> -->
					</view>
					<view class="buscardleft">
						<view class="context">
							<text class="">Easter</text>
							<text class="titletext">上海</text>
							<!-- <image class="buscardicon" src="../../../static/icon/nv.png" /> -->
						</view>
						<view class="context">
							<image class="buscardicon" style="margin-left: 0;" src="../../../static/icon/nv.png" />
							<text class="titletext">:国家电网公司</text>
						</view>
						<view class="context"><text class="titletext" style="margin-left: 0;">行业:电子商务</text></view>
						<view class="context"><text class="titletext" style="margin-left: 0;">需求:电子商务</text></view>
						<view class="context" style="margin-bottom: 10rpx;">
							<text class="titletext" style="margin-left: 0;">特长：</text>
							<text class="titletextadd">数据挖掘</text>
							<text class="titletextadd">网站开发</text>
							<text class="titletextadd" style="font-size: 33rpx;">+</text>
						</view>
					</view>
				</view>
			</div>
		</view>
		<view class="buscardBom">
			<view class="buscardBomtitle">
				<text style="	border-bottom:1px solid #81b991 ;padding-bottom: 5rpx;">个人信息</text>
			</view>
			<view class="buscardBomconnect">
				<div class="hm-friend-information-card">
					<view class="box2" style="margin-top: 25rpx;position: relative">
					<view class="context" style="font-size: 32rpx;padding: 5rpx;font-weight: 600;">
						联系方式
					</view>
					<view class="context">
						手机号：112345678901
					</view>
					<view class="context" style="margin-bottom: 25rpx;">
						微信号：112345678901
					</view>
					</view>
				</div>
				<div class="hm-friend-information-card">
					<view class="box2" style="margin-top: 15rpx;position: relative;">
					<view class="context">
						出生年月：2020/11/11
					</view>
					<view class="context" style="display: flex;">
						<text style="width: 250rpx;">我的标签:</text><text class="contexttext">的标签的标签的标签的标签的标签的标签的标签的标签的标签的标签的标签的标签的标签</text>
					</view>
					<view class="need" >
						<view class="" style="margin:15rpx 30rpx;">
							需求:
						</view>
						<view class="" style="margin-left: 30rpx;color: #82878a;margin-bottom: 25rpx;" >
							的标签的标签的标签的标签的标签的标签的标签的标签的标签的标标签的标签的标签的标签的标签的标签的标签的标签的标签的标签的标签的标签
						</view>
					</view>
					<view class="skill" >
						<view class="" style="margin:15rpx 30rpx;">
							技能:
						</view>
						<view class="" style="margin-left: 30rpx;color: #82878a;margin-bottom: 25rpx;" >
							的标签的标签的标签的标签的标签的标签的标签的标签的标签的标标签的标签的标签的标签的标签的标签的标签的标签的标签的标签的标签的标签
						</view>
					</view>
					</view>
				</div>
			</view>
			<view class="buscardBombutton">
				<view class="buttonadd" @click="addFriend">
					添加好友
				</view>
				<view class="buttonadd" @click="collectCard">
					收藏名片
				</view>
			</view>
		</view>
	</view>
</template>

<script>
export default {
	data() {
		return {
			productList: [],
			collected:false
		};
	},
	onLoad() {
		// console.log(getApp().globalData.tabindex);
		this.getbusinessCard();
	},
	methods: {
		getbusinessCard() {
			uni.request({
				url: 'https://api-hmugo-web.itheima.net/api/public/v1/home/swiperdata',
				success: res => {
					this.productList = res.data.message;
					console.log(this.productList);
				}
			});
		}
	},
	addFriend(){},
	collectCard(){
		// this.collected=true
		console.log("11")
	}
};
</script>

<style>
@import '../teaHouse/start.response.css';
@import '../teaHouse/business-card.css';
.box2{
	  margin-top: 25rpx;
	  display: flex;
	  /* align-self: center; */
	  flex-direction: column;
	
	  /* align-items: center; */
	  /* flex-direction: row; */
	  /* justify-content:center; */
	  /* border-radius: 38.96rpx; */
	  border-radius: 28rpx;
	  border: 1rpx solid rgba(209, 213, 223, 0.5);
	  box-shadow: 0px 10px 30px rgba(209, 213, 223, 0.5);
	  background-color: #ffffff;
	  /* width: 720.78rpx; */
	  width: 700rpx;
	  /* height: 233.77rpx; */
	
}
.titletextadd {
	display: inline-block;
	text-align: center;
	width: 135rpx;
	margin-left: 20rpx;
	font-size: 29rpx;
	background-color: #d2e6d7;
	padding-top: 15rpx;
	padding-bottom: 15rpx;
	border-radius: 7rpx;
}
.buscardBom{
	/* height: 270rpx; */
	margin-top: 20rpx;
	/* box-shadow: 0px 10px 30px rgba(209, 213, 223, 0.5); */
	 background-color: #ffffff;
	 font-size: 29rpx;
}
.buscardBomtitle{
	font-size: 27rpx;
	margin-left: 27rpx;
}
.contexttext{
	/* margin-top: -3rpx; */
	margin-left: 12rpx;
	margin-right: 5rpx;
	 -webkit-line-clamp: 3;
	 text-overflow: ellipsis;
	 display: -webkit-box;
	 -webkit-box-orient: vertical;
	overflow: hidden;
	/* line-height: 50rpx; */
}
.skill,.need{
	margin: 0 auto;
	font-size: 26rpx;
	background-color: #f1f6fa;
	width: 670rpx;
	border-radius: 5rpx;
	box-shadow: 0px 10px 30px rgba(209, 213, 223, 0.5);
}
.skill{
	margin-top: 15rpx;
	margin-bottom: 10rpx;
}
.buscardBombutton{
	height:80rpx ;
	margin-top: 45rpx;
	display: flex;
	flex-wrap: nowrap;
	justify-content: space-evenly;
	color: white;
}
.buttonadd{
	/* width: 200rpx;
	height: 100rpx;
	background-color: #81b991;
	text-align: center; */
	font-size:28rpx ;
	text-align: center;
	/* margin-right: 30rpx; */
	margin-top: -15rpx;
	background-color: #81B991;
	width: 190rpx;
	height: 70rpx;
	line-height: 70rpx;
	border-radius: 10rpx;
}
.collectcard{
	width: 130rpx;
	line-height: 50rpx;
	text-align: center;
	position: absolute;
	top:140rpx;
	right:67rpx;
	border: 1px solid black;
	background-color: #eeeeee;
	font-size: 29rpx;
}
</style>
