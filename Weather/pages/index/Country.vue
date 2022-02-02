<template>
	<view id="container">
		<view id="Title">
			<navigator url="Mannage">
				<image src="../Images/left.png" class="icon"></image>
			</navigator>
			<text class="add">添加城市</text>
		</view>
		<view class="seach"> </view>
		<view class="sustitle">推荐城市</view>
		<view class="coun">
			<view class="city">当前城市</view>
			<view class="city">北京</view>
			<view class="city">上海</view>
			<view class="city">广东</view>
			<view class="city">深圳</view>
			<view class="city">福建</view>
			<view class="city">合肥</view>
			<view class="city">宁夏</view>
			<view class="city">江西</view>
			<view class="city">海南</view>
			<view class="city">四川</view>
			<view class="city">西安</view>
			<view class="city">台湾</view>
			<view class="city">香港</view>
			<view class="city">青海</view>
			<view class="city">重庆</view>
			<view class="city">郑州</view>
			<view class="city">浙江</view>
			<view class="city">武汉</view>
			<view class="city">长沙</view>
			<view class="city">南昌</view>
			<view class="city">辽宁</view>
			<view class="city">内蒙古</view>
			<view class="city">....</view>
		</view>
	</view>
</template>

<script>
</script>

<style>
	#container{
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
	#Title .icon{
		width: 35px;
		height: 35px;
		position: absolute;
		top:2px;
	}
	#Title .add{
		width: 375px;
		height: 15px;
		font-size: 20px;
		color: #C0C0C0;
		position: absolute;
		top:4px;
		left:35px;
	}
	.seach{
		width: 375px;
		height: 30px;
		border: #555555 1px solid;
	}
	.sustitle{
		width: 375px;
		height: 40px;
		color:#007AFF;
		font-size: 18px;
		line-height: 40px;
		border: #555555 1px solid;
		padding-left: 10px;
	}
	.coun{
		width: 375px;
	}
	.city{
		width: 91px;
		height: 50px;
		line-height: 50px;
		font-size: 18px;
		color: #C0C0C0;
		text-align: center;
		display: inline-block;
		border: #666666 1px solid;
	}
</style>
