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
					id: "",
					name: "",
					sex: "",
					age: "",
				}
			}
		},
		watch: {
		  $route: {
		    handler: function(val, oldVal){
			  let res = this.$route.query.data;
			 
		      if (res) {
		      	this.addressData = res;
		      } else {
		      	this.addressData.id='',
		      	this.addressData.name='',
		      	this.addressData.sex='',
		      	this.addressData.age=''
		      }
		      
		    },
		    deep: true
		  }
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
