<template>
	<view>
		<input v-model="info.id" placeholder="输入id" />
		<br />
		<input v-model="info.name" placeholder="输入name" />
		<br />
		<input v-model="info.sex" placeholder="输入sex" />
		<br />
		<input v-model="info.age" placeholder="输入age" />
		<button @click="sava">SAVA</button>
		<navigator url="second">
			<button>AAAA</button>
		</navigator>
	</view>
</template>

<script>
	export default {
		data() {
			return {
				info: {
					id: "123",
					name: "GREAT",
					sex:"male",
					age:"18"
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
