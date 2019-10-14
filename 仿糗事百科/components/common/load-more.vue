<template>
	 <view class="load-more">{{items.loadtext}}</view>	  
</template>

<script>
	export default{
		props:{
			loadtext:String
		}
	}
</script>

<style scoped>
	.load-more{
	text-align:center;
	color:#aaaaaa;
	padding:15upx;
		
	}	
</style>
