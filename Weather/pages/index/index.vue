<template>
	<view id="container">
		<view class="Title">
			<navigator url="Mannage">
				<image src="../Images/city.png" class="urban"></image>
			</navigator>
			<text>Xianyou Country</text>
			<navigator url="Setting">
				<image src="../Images/set.png" class="set"></image>
			</navigator>
		</view>
		<view class="Temp">
			<view class="wd">14­°C</view>
			<view class="info">多云</view>
			<view class="info">19/13</view>
			<view class="info">空气良</view>
			<view class="company">中国天气通</view>
		</view>
		<view id="week">
			<view class="one">
				<text class="mon">3月4号周一</text>
				<image src="../Images/sun.png" class="icon"></image>
				<text class="mon_tem">24­°C/16­°C</text>
			</view>
			<view class="one">
				<text class="mon">3月5号周一</text>
				<image src="../Images/lei.png" class="icon"></image>
				<text class="mon_tem">28­°C/20­°C</text>
			</view>
			<view class="one">
				<text class="mon">3月6号周一</text>
				<image src="../Images/light.png" class="icon"></image>
				<text class="mon_tem">25­°C/17­°C</text>
			</view>
			<view class="one">
				<text class="mon">3月7号周一</text>
				<image src="../Images/sun.png" class="icon"></image>
				<text class="mon_tem">2­1°C/14°C</text>
			</view>
			<view class="one">
				<text class="mon">3月8号周一</text>
				<image src="../Images/rain.png" class="icon"></image>
				<text class="mon_tem">20°C/11°C</text>
			</view>
		</view>
		
		<!-- <uni-link :href="href" :text="href"></uni-link> -->
	</view>
</template>

<script>
	export default {
	    data() {
	        return {
	        }
	    },
	    methods: {
	    }
	}
</script>

<style>
	#container{
		width: 375px;
		background-color: #071E3D;
		margin: 0 auto;
	}
	.Title{
		width: 375px;
		height: 20px;
		font-size: 22px;
		text-align: center;
		margin-bottom: 5px;
		color: #F8F8F8;
		position: relative;
	}
	.Title .urban{
		width: 35px;
		height: 30px;
		position: absolute;
		left: 5px;
		top: 2px;
	}
	.Title .set{
		width: 35px;
		height: 30px;
		position: absolute;
		right: 5px;
		top: 2px;
	}
	.Temp{
		width: 375px;
		height: 200px;
		position: relative;
		margin-bottom: 5px;
	}
	.company{
		position: absolute;
		right: 2px;
		bottom: 0px;
		font-size: 12px;
		color: #808080;
	}
	.wd{
		font-size: 34px;
		text-align: center;
		margin: 20px 0px;
		color: #F8F8F8;
	}
	.info{
		text-align: center;
		margin-bottom: 5px;
		color: #C0C0C0;
	}
	#week .one{
		width: 372px;
		height: 50px;
		position: relative;
		border: #555555 1px solid;
	}
	#week .one .icon{
		width: 30px;
		height: 30px;
		position: absolute;
		top:10px;
		left:180px;
	}
	#week .one .mon{
		position: absolute;
		left: 5px;
		font-size: 18px;
		line-height: 50px;
		color: #C0C0C0;
	}
	#week .one .mon_tem{
		position: absolute;
		right: 5px;
		line-height: 50px;
		font-size: 18px;
		color: #C0C0C0;
	}
</style>
