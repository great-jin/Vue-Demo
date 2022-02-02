<template>
	<view >
	<w-article :articles="articles"></w-article>
	</view>
</template>

<script>
	import wArticle from '@/components/w-article/w-article.vue'
	export default {
		data() {
			return {
				title: 'Hello',
				articles: [{
					id: 1,
					title: '直戳欧盟痛点！法媒：中国不搞以牙还牙，直接加倍奉还',
					images: [],
					author: '新华社',
					type: '置顶'
				},
				{
					id: 2,
					title: '直戳欧盟痛点！法媒：中国不搞以牙还牙，直接加倍奉还',
					images: [],
					author: '新华社',
					type: '置顶'
				},
				{
					id: 3,
					title: '直戳欧盟痛点！法媒：中国不搞以牙还牙，直接加倍奉还',
					images: [],
					author: '新华社',
					type: '置顶'
				},
				{
					id: 4,
					title: 'LV官网男士夏日新品来袭 即刻在线选购',
					images: ['https://feed-image.baidu.com/0/pic/6d234cc4dfc71b12bef6f0bb702c3f11.jpg'],
					author: '路易威登中国官网',
					type: '广告'
				}
				,
				{
					id: 5,
					title: '这个是老鼠的断头台，哪里有老鼠放哪里，不过一次只能抓一只',
					images: ['https://feed-image.baidu.com/0/pic/6d234cc4dfc71b12bef6f0bb702c3f11.jpg'],
					author: '大自然奇妙物语',
					type: ''
				},
				{
					id: 6,
					title: '直戳欧盟痛点！法媒：中国不搞以牙还牙，直接加倍奉还',
					images: ['https://feed-image.baidu.com/0/pic/6d234cc4dfc71b12bef6f0bb702c3f11.jpg','https://feed-image.baidu.com/0/pic/6d234cc4dfc71b12bef6f0bb702c3f11.jpg','https://feed-image.baidu.com/0/pic/6d234cc4dfc71b12bef6f0bb702c3f11.jpg'],
					author: '大自然奇妙物语',
					type: ''
				},
				{
					id: 7,
					title: 'LV官网男士夏日新品来袭 即刻在线选购',
					images: ['https://feed-image.baidu.com/0/pic/6d234cc4dfc71b12bef6f0bb702c3f11.jpg'],
					author: '路易威登中国官网',
					type: '广告'
				}
				,
				{
					id: 8,
					title: 'LV官网男士夏日新品来袭 即刻在线选购',
					images: ['https://feed-image.baidu.com/0/pic/6d234cc4dfc71b12bef6f0bb702c3f11.jpg'],
					author: '路易威登中国官网',
					type: '广告'
				}
				,]
			}
		},
		onLoad() {

		},
		methods: {

		},
		components:{
			wArticle
		}
	}
</script>

<style>
	
</style>
