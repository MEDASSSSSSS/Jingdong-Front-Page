<template lang="html">
	<Panel title="新手特权" :class="$style.panel">
		<section :class="$style.content">
			<div :class="$style.item">
				<h4>下载APP<span :class="$style.red">送888元礼包</span></h4>
				<p>新手专享</p>
				<img src="//misc.360buyimg.com/mtd/pc/common/img/no_login.jpg" alt="新手专享">
			</div>
			<div :class="$style.item">
				<ul>
					<li>
						<img src="//misc.360buyimg.com/mtd/pc/common/img/no_login.jpg" alt="">
						<div :class="$style.left">
							<p :class="$style.red">领128元新手礼包</p>
							<router-link :to="{name:'home'}"><p>立即开通</p></router-link>
						</div>
					</li>
					<li>
						<img src="//misc.360buyimg.com/mtd/pc/common/img/no_login.jpg" alt="">
						<div :class="$style.left">
							<p>打白条<span :class="$style.red">享免息</span></p>
							<router-link :to="{name:'home'}"><p>立即开通享豪礼</p></router-link>
						</div>
					</li>
				</ul>
			</div>
		</section>
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
	>h4{
		border-bottom:1px solid #ddd;
	}
	.content{
		@include list;
		.item{
			width:50%;
			font-size:24px;
			box-sizing:border-box;
			&:first-child{
				padding:32px 20px;
				text-align:center;
				border-right:1px solid #ddd;
			}
			h4 + p {
				margin: 10px 0;
				line-height:40px;
			}
			.red{
				color:#f00;
			}
			ul{
				width:100%;
				li{
					width:100%;
					height:144px;
					padding:32px 28px;
					box-sizing:border-box;
					&:first-child{
					border-bottom:1px solid #ddd;
					}
					p{
						white-space:nowrap;
						text-overflow:ellipsis;
						overflow:hidden;
						margin:6px;
					}
					a{
						text-decoration:none;
						color:#999;
					}
					img{
						float:right;
						width:80px;
						height:80px;
					}
				}
			}
			
		}
		
		
	}
	

}
	
</style>