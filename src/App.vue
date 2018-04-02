<template>
  <div id="app">
    <v-head></v-head>
    <div id="tab">
		<div class="tab-item" border-1px>
			<router-link to= '/goods'>商品</router-link>
		</div>
		<div class="tab-item">
			<router-link to= '/ratings'>评价</router-link>
		</div>
		<div class="tab-item">
			<router-link to='/seller'>商家</router-link>
		</div>
		<router-view></router-view>
	</div>
  </div>
</template>

<script>
import Head from './components/header/header.vue'

export default {
  name: 'App',
  components: {
    'v-head': Head
  }
}
</script>

<style lang="less">
	@import 'common/less/border';
	
	#tab{
		display: flex;
		width:100%;
		height:40px;
		line-height:40px;
		.tab-item{
			flex:1;
			flex-direction: row;
			text-align: center;
			.border-1(rgba(7,17,27,0.1));
		}
		a{
			display: block;
			color:rgb(77,85,93);
			font-size:14px;
		}
		.router-link-active{
			color:rgb(240,20,20)
		}
	}
</style>
