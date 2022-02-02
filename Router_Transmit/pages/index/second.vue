<template>
	<view id="AA">
		<view>id:{{addressData.id}}</view>
		<view>name:{{addressData.name}}</view>
		<view>sex:{{addressData.sex}}</view>
		<view>age:{{addressData.age}}</view>
		<navigator url="index">
			<button>跳转到新页面并传参</button>
		</navigator>
	</view>
</template>

<script>
	export default {
		data() {
			return {
				addressData: {
					id: "110",
					name: "110",
					sex: "110",
					age: "110",
				}
			}
		},
		methods: {},
		watch: {
		  $route: {
		    handler: function(val, oldVal){
			  let res = this.$route.query.data;
			 
		      if (res) {
		      	this.addressData = res;
		      } else {
		      	this.addressData.id='110',
		      	this.addressData.name='110',
		      	this.addressData.sex='110',
		      	this.addressData.age='110'
		      }
		      
		    },
		    deep: true
		  }
		},
		onLoad: function() {
			// let res = this.$route.params.data;
			// console.log(res==null)
			// if (res) {
			// 	this.addressData = res;
			// } else {
			// 	this.addressData.id='110',
			// 	this.addressData.name='110',
			// 	this.addressData.sex='110',
			// 	this.addressData.age='110'
			// }

			// console.log(res)
		}
	}
</script>

<style>
	#AA {
		width: 360px;
		margin: 0 auto;
		border: #007AFF 3px solid;
	}

	#AA view {
		width: 250px;
		height: 50px;
		color: #3B4144;
		margin: 5px auto;
		font-size: 22px;
	}
</style>
