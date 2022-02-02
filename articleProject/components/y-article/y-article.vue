<template>
	<view>
		<view class="article-list" v-for="item in  articles" :key="item.id">
			<view class="article" v-if="item.images.length==1">
				<view class="article-1" v-if="item.type=='广告'">
					<view class="article-title">{{item.title|shorten}}</view>
					<view class="article-img">
						<image style="width: 100%; margin-top: 10px;" :src="item.images[0]" mode="widthFix"></image>
					</view>
					<view class="article-bars">
						<text>{{item.author}}</text>
						<text style="margin-left: 10px;">{{item.type}}</text>
					</view>
				</view>
				<view class="article-2" v-if="item.type!='广告'">
					<view class="article-img">
						<image style="width: 100px;height: 100px;"  :src="item.images[0]" mode="widthFix"></image>
					</view>
					<view class="article-content">
						<view class="article-title">{{item.title|shorten}}</view>
						<view class="article-bars">
							<text>{{item.author}}</text>
						</view>
					</view>
				</view>
			</view>
		</view>
	</view>
</template>

<script>
	export default {
		name: "y-article",
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
			shorten(value){
				if(value.length>30){
					return value.substring(0,29)+'...'
				}
				else{
					return value
				}
			}
		}
	}
</script>

<style>
	.article{
		padding:10px;
		border-bottom: 1px solid #eae9ee;
	}
	 .artcle-title{
		font-size: 18px;
		color: #333;
	}
	.article-bars{
		font-size: 10px;
		color: #C8C7CC;
	}
	.article-1 .artcle-title{
		margin-bottom: 5px;
	}
	.article-2{
		display: flex;
	}
	.article-2 .article-content{
		padding-left: 20px;
		position: relative;
	}
	.article-2 .article-bars{
		position: absolute;
		bottom: 0;
		left: 20px;
	}
</style>
