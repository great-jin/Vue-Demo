<template>
	<view>
		<input v-model="info.id" placeholder="输入id" />
		<input v-model="info.name" placeholder="输入name" />
		<input v-model="info.sex" placeholder="输入sex" />
		<input v-model="info.age" placeholder="输入age" />
		<button @click="sava">SAVA</button>
		<navigator url="second">
			<button>Transmit</button>
		</navigator>
	</view>
</template>

<script>
	import datas from '../data/datas.js'
	export default {
		data() {
			return {
				info: {
					id: "",
					name: "",
					sex:"",
					age:""
				}
			}
		},
		methods: {
			sava() {
				datas.id = this.info.id;
				datas.name = this.info.name;
				datas.sex = this.info.sex;
				datas.age = this.info.age;
			}
		}
	}
</script>

<style>

</style>
