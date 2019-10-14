<template>
	<view class="uni-tab-bar">
			 <scroll-view scroll-x class="uni-swiper-tab">
				 <view class="swiper-tab-list">
				  <block v-for="(tab,index) in tabBars" :key="tab.id">
					<view class="swiper-tab-list" :class="{'active':tabIndex==index}" @tap="tabtap(index)">
					 	{{tab.name}}
					  <view class="swiper-tab-line" :class="{'active':tabIndex==index}"></view>	
					</view>  
				  </block>	 
				 </view>
			 </scroll-view> 
	</view>
</template>

<script>
	export default{
		props:{
		  tabBars:Array,
			  tabIndex:Number
		},
		 methods:{
			 tabtap(index){
			 	this.$emit('tabtap',index);
			 },
		 }
	}
</script>

<style>
	.uni-swiper-tab{
		border-bottom:1upx solid #eeeeee;
	}
	 .swiper-tab-list{
		color:#969696;
		font-weight:bold;
	 }
	 .uni-tab-bar .active{
		 color:#343434;
	 }
	 .active .swiper-tab-line{
		 border-bottom:6upx solid #fede33;
		 width:70upx;
		 margin: auto;
		 border-top:6upx solid #fede33;
		 border-radius:20upx;
	 }
</style>
