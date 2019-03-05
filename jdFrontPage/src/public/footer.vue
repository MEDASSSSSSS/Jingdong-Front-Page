<template lang="html">
	<Panel title='公司信息' :cname="$style.panel">
		<ul :class="$style.content">
			<li>
				<router-link :to="{name:'home'}">
					<p>在线客服</p>
				</router-link>
			</li>
			<li>
				<div><img src="//misc.360buyimg.com/mtd/pc/common/img/no_login.jpg" alt="">客户端</div>
				<div><img src="//misc.360buyimg.com/mtd/pc/common/img/no_login.jpg" alt="">触屏版</div>
				<div><img src="//misc.360buyimg.com/mtd/pc/common/img/no_login.jpg" alt="">电脑版</div>
			</li>
			<li>Copyright 2004-2018</li>
			<li>投资有风险，购买需谨慎</li>
			<li>金融平台服务协议</li>
			<li>金融隐私政策</li>
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
	margin-top:20px;
	margin-bottom:100px;
	background-color:#f5f5f5;
	>h4{
		display:none;
	}
	.content{
		@include flex;
		li{
			text-align:center;
			color:#999;
			font-size:24px;
			a{
				text-decoration:none;
				color:#333;
				text-align:center;
				
				p{
					padding:10px 0;
					background-color:#fff;
				}
			}
			&:nth-child(2){
				@include flex(row);
				box-sizing:border-box;
				height:186px;
				>div{
					width:33.3333%;
					text-align:center;
					font-size:24px;
					color:#666;
					white-space:no-wrap;
					text-overflow:ellipsis;
					overflow:hidden;
					img{
						display:block;
						width:90px;
						height:90px;
						margin:20px auto;
						border-radius:50%;
					}

				}
			}
			&:nth-child(n+3){
				padding:20px 0;
				line-height:38px;
				border-top:1px solid #ddd;
			}
		}
	}

}
</style>