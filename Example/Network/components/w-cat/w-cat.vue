<template>
	<view>
		<scroll-view scroll-x="true" class="cats">
			<view class="cat-item" v-for="item in cats" :key="item.cat_id">{{item.cat_name}}</view>
		</scroll-view>
	</view>
</template>

<script>
	export default {
		props:{
			cats:{
				type:Array,
				required:true
			}
		},
		data() {
			return {
				
			};
		}
	}
</script>

<style>
	.cats{
		height: 80rpx;
		line-height: 80rpx;
		white-space: nowrap;
		border-bottom:1rpx solid #C8C7CC ;
	}
	.cat-item{
		display: inline;
		margin: 0 20rpx;
		/* width: 200rpx;
		height: 50rpx;
		line-height: 50rpx;
		text-align: center; */
	}

</style>
