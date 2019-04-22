<template>
	<view class="content">
		—————————————————————————————— 事件  和VUE一样——————————————————————————————
      <input type="text" value="" 
		style="background: #8F8F94;height:100upx;"
		@input="change"
		@focus="focus"
		@blur="blur"
		@confirm="confirm"
		@tap="tap"
		@longpress="longpress"
	   />
	   <!--——————————————————————————————————Vif—————————————————————————————————————————— -->
	   <view class="" v-if="isShow">now you see me</view>
	</view>
</template>
<script>
	export default {
		data() {
			return {
			isShow:true,
			}
		},
		onLoad() {
          // #ifdef H5
			console.log('在H5端编译')
			// #endif
			// #ifdef APP-PLUS
			console.log('在APP端编译')
			// #endif
		},
		methods: {
			change(){
				console.log('输入框输入')
			},
			focus(){
				console.log('得到焦点')
			},
			blur(){
				console.log('失去焦点')
			},
			confirm(){
				console.log('组件单击事件')
			},
			tap(){
				console.log('组件被触摸')
			},
			longpress(){
				console.log('长时间按住')
			},
			
		}
	}
</script>

<style>
	.content {
		text-align: center;
		height: 400upx;
	}
    .logo{
        height: 200upx;
        width: 200upx;
        margin-top: 200upx;
    }
	.title {
		font-size: 36upx;
		color: #8f8f94;
	}
</style>
