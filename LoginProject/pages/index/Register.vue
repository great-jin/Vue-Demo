<template>
	<view id="content">
		<view class="info">

			<view style="border-top:#C0C0C0 2upx solid">
				<view style="margin:30px;"></view>
				<text class="baner"  style="margin:10px;">账号：</text>
				<br/>
				<view>
					<uni-easyinput v-model="addressData.name" class="tt" />
				</view>
			</view>

			<view>
				<text class="baner" style="margin:10px ;">密码：</text>
				<br/>
				<view>
					<uni-easyinput v-model="addressData.pwd" class="tt" />
				</view>
			</view>
			<button @click="register" class="sava">注册</button>

		</view>
	</view>
</template>

<script>
	import datas from '../datas.js'
	export default {
		data() {
			return {
				value: '',
				item: '',
				title: 'picker',
				addressData: {
					name: '',
					pwd: ''
				}
			}
		},
		methods: {
			register() {
				datas.id = this.addressData.name;
				datas.name = this.addressData.pwd;
				uni.redirectTo({
					url: 'index'
				});
			}
		}
	}
</script>

<style>
	* {
		margin: 0px;
		padding: 0px;
	}
	#content {
		display: flex;
		flex-direction: column;
	}
	.baner{
		display: inline-block;
		height: 20px;
	}
	.sava {
		margin-top: 10px;
	}
</style>
