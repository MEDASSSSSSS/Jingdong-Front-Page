<template lang="html">
	<Panel title="导航条" :cname="$style.panel">
		<ul :class="$style.content">
			<li><router-link :to="{name:'home'}"><img src="//misc.360buyimg.com/mtd/pc/common/img/no_login.jpg" alt=""><p>首页</p></router-link></li>
			<li><router-link :to="{name:'home'}"><img src="//misc.360buyimg.com/mtd/pc/common/img/no_login.jpg" alt=""><p>理财</p></router-link></li>
			<li><router-link :to="{name:'home'}"><img src="//misc.360buyimg.com/mtd/pc/common/img/no_login.jpg" alt=""><p>白条</p></router-link></li>
			<li><router-link :to="{name:'home'}"><img src="//misc.360buyimg.com/mtd/pc/common/img/no_login.jpg" alt=""><p>众筹</p></router-link></li>
			<li><router-link :to="{name:'home'}"><img src="//misc.360buyimg.com/mtd/pc/common/img/no_login.jpg" alt=""><p>我的</p></router-link></li>
		</ul>
	</Panel>

</template>
<script>
	import Panel from '../components/panel.vue'
	export default{
		components:{
			Panel,

		}
	}

</script>
<style lang="scss" module>
@import "../assets/element.scss";
.panel{
	@include panel;
	position:fixed;
	bottom:0;
	left:0;
	right:0;
	height:100px;
	z-index:10;
	>h4{
		display:none;
	}
	.content{
		@include flex(row);
		justify-content:space-around;
		li{
			text-align:center;
			a{
				text-decoration:none;
				font-size:22px;
				color:#656565;
				img{
					width:44px;
					height:44px;
					display:inline-block;
					margin:12px auto 6px;
				}
				p{
					font-size:22px;
				}
			}
		}
	}
}
</style>