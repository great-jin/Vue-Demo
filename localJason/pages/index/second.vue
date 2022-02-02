<template>
	<view>
		<text>{{info.id}}</text>
		<br />
		<text>{{info.name}}</text>
		<br />
		<text>{{info.sex}}</text>
		<br />
		<text>{{info.age}}</text>
	</view>
</template>

<script>
	import datas from '../data/datas.js'
	export default {
		data() {
			return {
				title: 'Hello',
				info: {
					id: '',
					name: '',
					sex: '',
					age:''
				}
			}
		},
		onShow() {
			if(datas){
				this.info.id = datas.id;
				this.info.name = datas.name;
				this.info.sex= datas.sex;
				this.info.age = datas.age;
				
			}
		},
		methods: {
		},
	}
</script>

<style>
</style>
