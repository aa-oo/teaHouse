<template>
	<view class="">
			<view class="top">
			<view class="articletop">文章详情</view>
			<view class="articleauthor">文章详情</view>
			<view class="articletime">文章详情</view>
			</view>
			<view class="bottom">
				<view class="articlecontect">
					文章详情文章详情文章详情文章详情文章详情v文章详情文章详情v文章详情文章详情v文章详情文章详情v文章详情v文章详情vv文章详情v文章详情v文章详情文章详情vv文章详情vv文章详情文章详情vv文章详情文章详情v文章详情文章详情v文章详情文章详情vv文章详情文章详情v文章详情文章详情v文章详情文章详情vvv文章详情
						文章详情文章详情文章详情文章详情文章详情v文章详情文章详情v文章详情文章详情v文章详情文章详情v文章详情v文章详情vv文章详情v文章详情v文章详情文章详情vv文章详情vv文章详情文章详情vv文章详情文章详情v文章详情文章详情v文章详情文章详情vv文章详情文章详情v文章详情文章详情v文章详情文章详情vvv文章详情
						文章详情文章详情文章详情文章详情文章详情v文章详情文章详情v文章详情文章详情v文章详情文章详情v文章详情v文章详情vv文章详情v文章详情v文章详情文章详情vv文章详情vv文章详情文章详情vv文章详情文章详情v文章详情文章详情v文章详情文章详情vv文章详情文章详情v文章详情文章详情v文章详情文章详情vvv文章详情
						文章详情文章详情文章详情文章详情文章详情v文章详情文章详情v文章详情文章详情v文章详情文章详情v文章详情v文章详情vv文章详情v文章详情v文章详情文章详情vv文章详情vv文章详情文章详情vv文章详情文章详情v文章详情文章详情v文章详情文章详情vv文章详情文章详情v文章详情文章详情v文章详情文章详情vvv文章详情
						文章详情文章详情文章详情文章详情文章详情v文章详情文章详情v文章详情文章详情v文章详情文章详情v文章详情v文章详情vv文章详情v文章详情v文章详情文章详情vv文章详情vv文章详情文章详情vv文章详情文章详情v文章详情文章详情v文章详情文章详情vv文章详情文章详情v文章详情文章详情v文章详情文章详情vvv文章详情
				</view>

			</view>
			<!-- {{item.titlename}} -->
	</view>
</template>

<script>
	export default{
		data() {
			return {};
		},
		onLoad() {
			uni.setNavigationBarTitle({
			    title:'安徽合肥官方'
			})
		},
		// props:['item.titlename']
		methords(){
			
		}
	}
</script>

<style>
	.top{
		border-top: 1px solid #3f6a4b;
		text-align: center;
	}
	.articletop{
		margin-top: 15rpx;
	    font-style: italic;
		font-weight: bold;
		font-size: 45rpx;
	}
	.articleauthor{
		margin-top: 50rpx;
		font-size: 37rpx;
	}
	.articletime{
		margin-top: 15rpx;
		font-size: 38rpx;
	}
	.bottom{
		margin-top: 50rpx;
		font-size: 32rpx;
	}
	.articlecontect{
		padding-bottom: 40rpx;
	}
	
</style>
