<template>
	<view>
		<view class="article-list" v-for="item in  articles" :key="item.id">
			
			<view class="article-1" v-if="item.images.length==0">
				<view class="article-title">
					{{item.title|shorten}}
				</view>
				<view class="article-bars">
					<text class="top">{{item.type}}</text>
					<text class="author">{{item.author}}</text>
				</view>
			</view>

			<view class="article-2" v-if="item.images.length==1">
				<view class="article-2-1" v-if="item.type=='广告'">
					<view class="article-title">{{item.title|shorten}}</view>
					<view class="article-img">
						<image style="width: 100%;" :src="item.images[0]" mode="widthFix"></image>
					</view>
					<view class="article-bars">
						<text>{{item.author}}</text>
						<text>{{item.type}}</text>
					</view>
				</view>
				<view class="article-2-2" v-if="item.type!='广告'">
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


			<view class="article-3" v-if="item.images.length==3">
				<view class="article-title">
					{{item.title|shorten}}
					
				</view>
				<view class="article-imgs" >
					<image :src="item" mode="widthFix" v-for="item in item.images"></image>
				</view>
				<view class="article-bars">
					<text>{{item.author}}</text>
				</view>
			</view>
		</view>
	</view>
</template>

<script>
	export default {
		name: "w-article",
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
				if(value.length>24){
					return value.substring(0,23)+'...'
				}
				else{
					return value
				}
				
				
			}
			
		}
	}
</script>

<style>
	.article-1, .article-2, .article-3{
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
	.article-1 text{

		font-size: 10px;
		color: #C8C7CC;
	
	}
	.article-1 .author{
		margin-left:10px;
	}
	.article-1 .artcle-title{
		margin-bottom: 10px;
	}
	.article-1 .top{
		color: red;
	}
	.article-1 .author{
		margin-left: 10px;
	}  
	.article-2-1 .artcle-title{
		margin-bottom: 5px;
	}
	.article-2-2{
		display: flex;
	}
	.article-2-2 .article-content{
		padding-left: 20px;
		position: relative;
	}
	.article-2-2 .article-bars{
		
		position: absolute;
		bottom: 0;
		left: 20px;
		
	}
	.article-3 .article-imgs{
		display: flex;
		flex-direction: row;
		
		
	}
	.article-3 .article-imgs image{
		height:100px;
		flex: 1;
		border: 1px solid white;
	}

</style>
