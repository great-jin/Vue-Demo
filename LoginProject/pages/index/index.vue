<template>
	<view>
		<form @submit="formSubmit" @reset="formReset" class="login">

			<view style="margin-top: 20px; margin-left: 10px;">用户名：</view>
			<view class="uni-form-item uni-column login-item"
				style="margin-top: 10px;margin-left: 10px;margin-right: 10px;">
				<input class="uni-input" name="name" placeholder="请输入用户名称" />
			</view>

			<view style="margin-top: 20px; margin-left: 10px;">密码：</view>
			<view class="uni-form-item uni-column login-item"
				style="margin-top: 10px; margin-left: 10px;margin-right: 10px;">
				<input class="uni-input" password="true" name="password" placeholder="请输入用户密码" />
			</view>

			<view class="uni-btn-v  login-submit" style="margin-top: 50px;">
				<button form-type="submit">登录</button>
				<button type="default" form-type="reset">重置</button>
			</view>
		</form>

		<view class="login-tools" style="margin-top: 300px;">
			<navigator url="Register">
				<view class="tools register">用户注册</view>
			</navigator>
		</view>
	</view>
</template>

<script>
	export default {
		data() {
			return {}
		},
		onLoad() {},
		computed: {},
		methods: {
			formSubmit: function(e) {
				let that = this;
				let {
					name,
					password
				} = e.detail.value

				uni.request({
					url: 'http://localhost:7001',
					method: 'POST',
					data: {
						name: name,
						password: password
					},
					success: function(res) {
						if (res.data.code == 1) {
							uni.redirectTo({
								url: 'second'
							});
							console.log(res.data.msg)
						} else {
							uni.showToast({
								title: '用户名和密码错误',
								duration: 2000,
							});
							console.log(res.data.msg)
						}
					}
				})
			},
			formReset: function(e) {
				console.log('清空数据')
			}
		}
	}
</script>

<style>
	.login-item {
		margin-bottom: 20rpx;
		border: 1rpx solid #a3a3a3;
		height: 70rpx;
		border-radius: 20rpx;
		line-height: 70rpx;
	}

	.login-submit {
		display: flex;
	}

	.login-submit button {
		width: 50%;
	}

	.login-tools {
		display: flex;
		height: 70rpx;
	}

	.login-tools .tools {
		line-height: 70rpx;
		flex: 1;
		text-align: center;
	}
</style>
