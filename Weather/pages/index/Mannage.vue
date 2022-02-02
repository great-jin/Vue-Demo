<template>
	<view id="container">
		<view id="Title">
			<navigator url="index">
				<image src="../Images/left.png" class="icon"></image>
			</navigator>
			<text class="add">管理城市</text>
		</view>
		<view class="city">
			<view class="xy">Xianyou Country</view>
			<image src="../Images/local.png" class="icon"></image>
			<view class="temp">14­°C</view>
		</view>
		<view class="add">
			<navigator url="Country">
				<view class="addCity">添加城市</view>
			</navigator>
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
	.city{
		width: 370px;
		height: 80px;
		position: relative;
		border: #808080 1px solid;
	}
	.city .icon{
		width: 30px;
		height: 30px;
		position: absolute;
		top:24px;
		left: 198px;
	}
	.city .xy{
		height: 80px;
		line-height: 80px;
		display: inline-block;
		font-size: 23px;
		color: #DCDFE6;
		padding-left: 10px;
	}
	.city .temp{
		height: 80px;
		line-height: 80px;
		display: inline-block;
		font-size: 30px;
		position: absolute;
		color: #DCDFE6;
		right: 7px;
		padding-left: 10px;
	}
	.add{
		width: 200px;
		height: 60px;
		margin: 0 auto;
		
	}
	.add .addCity{
		color: #F8F8F8;
		font-size: 20px;
		text-align: center;
		margin-top: 460px;
		border: 1px solid #DCDFE6;
	}
</style>
