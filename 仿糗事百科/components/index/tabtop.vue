<template>
				<view class="nav_top"  :style="{height:headHeight+'px'}">
					<view class="statusBar" :style="{height:statusBarHeight+'px'}"></view>
					<view>sdsdsdsd5454</view>
				</view>
</template>

<script>
	export default{
		  data(){
			  return{
			  statusBarHeight:"",
			  headHeight:"",
		  }
		  },
		created(){
	        const system = uni.getSystemInfoSync()
	   		this.statusBarHeight = system.statusBarHeight || 25
	   		this.headHeight = (system.statusBarHeight || 25) + 45//可调整
		}
	}
</script>
  

<style>
.nav_top{
  background:red;	
}	
</style>
