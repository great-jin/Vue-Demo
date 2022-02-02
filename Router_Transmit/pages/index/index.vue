<template>
	<view class="content">
		<input v-model="addressData.id" placeholder="输入id"/>
		<br />
		<input v-model="addressData.name" placeholder="输入name"/>
		<br />
		<input v-model="addressData.sex" placeholder="输入sex"/>
		<br />
		<input v-model="addressData.age" placeholder="输入age"/>
		<br />
		<button @click="jump">跳转到新页面并传参</button>
		<br />
	</view>
</template>

<script>
	export default {
		data() {
			return {
				addressData: {}
			}
		},
		methods: {
			jump() {
				this.$router.push({
					path:'/pages/index/second',
					query:{
						data: this.addressData
					}
					 // params:{
						//  data: this.addressData
						//  },
					});
			}
		}
	}
</script>

<style>
	.content {
		display: flex;
		flex-direction: column;
		align-items: center;
		justify-content: center;
	}
</style>
