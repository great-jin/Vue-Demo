<template>
	<view >
	   <w-cat :cats="cats"></w-cat>
	   <w-article :articles="articles"></w-article>
	</view>
</template>

<script>
	export default {
		data() {
			return {
				title: 'Hello',
				cats:[],
				articles:[]
			}
		},
		onLoad() {
			let that =this;//vue对象
			//异步操作
			uni.request({
				url:"http://lshop.cn.utools.club/api/articlecate/getmobilearticlecates",
				success:function(res){
					//this uni对象
					that.cats=res.data;
				
				}
				
			})
			uni.request({
				url:'https://qzimp.cn/api/articles/open',
				success: (res) => {
					that.articles=res.data;
				}
			})
			
		
		},
		methods: {

		}
	}
</script>

<style>
	
</style>
