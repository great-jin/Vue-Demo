<template>
	<view class="article-list">
		<view class="article" v-for="item in articles" :key="item.article_id">
			<view class="article-img">
				<image  :src="item.thumb" lazy-load="true" mode="scaleToFill"></image>
			</view>
			<view class="article-content">
				<view class="article-title">
					{{item.title|formatString}}
				</view>
				<view class="article-tools">
					<text class="article-catId">{{item.cat_id}}</text>
					<text class="article-author">{{item.author}}</text>
					<text class="article-time">{{item.add_time|formatDate}}</text>
				</view>
			</view>
		</view>
		
	</view>
</template>

<script>
	export default {
		props:{
			articles:{
				type:Array,
				required:true
			}
		},
		data() {
			return {
				
			};
		},
		filters:{
			formatDate(value){
				var date = new Date(value*1000);
				  var y = date.getFullYear(),
				    m = date.getMonth() + 1,
				    d = date.getDate(),
				    h = date.getHours(),
				    i = date.getMinutes(),
				    s = date.getSeconds();
				  if (m < 10) { m = '0' + m; }
				  if (d < 10) { d = '0' + d; }
				  if (h < 10) { h = '0' + h; }
				  if (i < 10) { i = '0' + i; }
				  if (s < 10) { s = '0' + s; }
				  var t = y + '-' + m + '-' + d;
				  return t;
	
			},
			formatString(value){
				let str=''
				if(value.length>30){
					str=value.substring(0,30)+'...'
				}
				else{
					str=value
				}
				return str;
				
			}
		}
	}
</script>

<style>
	.article{
		display: flex;
		padding: 0 10rpx;
		margin: 20rpx 0;
		height: 180rpx;
		
	}
	.article-img{
		
	}
	.article-img image{
		width: 240rpx;
		height: 180rpx;
	}
	.article-content{
		margin-left: 20rpx;
		font-size: 36rpx;
		position: relative;
	}
	.article-tools {
		position: absolute;
		left: 0;
		top: 136rpx;
	}
	.article-tools text{
		margin: 0 10rpx;
		font-size: 14rpx;
	
	}

</style>
