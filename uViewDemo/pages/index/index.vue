<template>
	<view class="">
		<u-form :model="user" ref="uForm">
			<u-form-item label="姓名" prop="name">
				<u-input v-model="user.name" />
			</u-form-item>
			<u-form-item label="密码" prop="password">
				<u-input type="password" v-model="user.password" />
			</u-form-item>
		</u-form>
		<u-button @click="submit">提交</u-button>
	</view>
</template>

<script>
export default {
	data() {
		return {
			user: {
				name: '',
				password: '',
			},
			rules: {
				name: [
					{ 
						required: true, 
						message: '请输入姓名', 
						trigger: ['change','blur'],
					}
				],
				password: [
					{
						required: true,
						message: '请输入密码', 
						trigger: ['change','blur'],
					}
				]
			}
		};
	},
	methods: {
		submit() {
			this.$refs.uForm.validate(valid => {
				if (valid) {
					console.log('验证通过');
					console.log(this.user);
				} else {
					console.log('验证失败');
				}
			});
		}
	},
	onReady() {
		this.$refs.uForm.setRules(this.rules);
	}
};
</script>