<template>
	<view id="container">
		<view id="Title">
			<navigator url="index">
				<image src="../Images/left.png" class="icon"></image>
			</navigator>
			<text class="add">设置</text>
		</view>
		<view class="pe">
			<text class="con">温度单位:</text>
			<text class="conn">°C</text>
		</view>
		<view class="pe">
			<text class="con">天气声音</text>
			<switch :checked="Values" />
		</view>
		<view class="pe">
			<text class="con">自动更新</text>
			<switch :checked="Values" />
		</view>
		<view class="pe">
			<text class="con">时间间隔</text>
		</view>
		<view class="pe">
			<text class="con">关于</text>
		</view>
	</view>
</template>

<script>
	export default {
		data() {
			return {
				Values: true
			}
		},
		methods: {}
	}
</script>

<style>
	#container {
		width: 375px;
		height: 670px;
		margin: 0 auto;
		background-color: #071E3D;
	}

	#Title {
		width: 375px;
		height: 50px;
		position: relative;
	}

	#Title .icon {
		width: 35px;
		height: 35px;
		position: absolute;
		top: 2px;
	}

	#Title .add {
		width: 375px;
		height: 15px;
		font-size: 20px;
		color: #C0C0C0;
		position: absolute;
		top: 4px;
		left: 35px;
	}

	.pe {
		width: 372px;
		height: 60px;
		border: #555555 1px solid;
	}

	.pe switch {
		width: 50px;
		height: 30px;
		margin-left: 220px;
	}

	.pe .con {
		height: 60px;
		line-height: 60px;
		padding-left: 10px;
		color: #DCDFE6;
		font-size: 20px;
		display: inline-block;
	}

	.pe .conn{
		height: 60px;
		line-height: 60px;
		padding-left: 10px;
		color: #DCDFE6;
		font-size: 24px;
		padding-left: 220px;
		display: inline-block;
	}
</style>
