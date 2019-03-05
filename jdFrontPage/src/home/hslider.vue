<template lang="html">
	<article class="">
		<Slider :items="items" :cname="$style.slider"/>
		<section :class="$style.list">
			<div :class="$style.item" v-for="item in enters" :key="item.img">
				<router-link :to="{name:item.href}">
					<img :src="item.img" :alt="item.title">
					<h4>{{item.title}}</h4>
				</router-link>
			</div>
		</section>
	</article>
	
</template>
<script>
	import Slider from "../components/slider.vue"
	export default{
		components:{
			Slider,
		},
		data(){
			return {
				items:[{
					href:"home",
					src:"//m.360buyimg.com/babel/jfs/t1/25307/24/8822/93279/5c78cf39E94e4a433/1cd227109d81bc90.jpg"
				},{
					href:"home",
					src:"//m.360buyimg.com/babel/jfs/t1/25307/24/8822/93279/5c78cf39E94e4a433/1cd227109d81bc90.jpg"
				},{
					href:"home",
					src:"//m.360buyimg.com/babel/jfs/t1/25307/24/8822/93279/5c78cf39E94e4a433/1cd227109d81bc90.jpg"
				},{
					href:"home",
					src:"//m.360buyimg.com/babel/jfs/t1/25307/24/8822/93279/5c78cf39E94e4a433/1cd227109d81bc90.jpg"
				}
				],
				enters:[{
					href:"home",
					img:"//misc.360buyimg.com/mtd/pc/common/img/no_login.jpg",
					title:"优惠券",
				},{
					href:"home",
					img:"//misc.360buyimg.com/mtd/pc/common/img/no_login.jpg",
					title:"领红包",
				},{
					href:"home",
					img:"//misc.360buyimg.com/mtd/pc/common/img/no_login.jpg",
					title:"抢钢镚",
				},{
					href:"home",
					img:"//misc.360buyimg.com/mtd/pc/common/img/no_login.jpg",
					title:"领京豆",
				},{
					href:"home",
					img:"//misc.360buyimg.com/mtd/pc/common/img/no_login.jpg",
					title:"白条提醒",
				}],
			}
		}
	}

</script>
<style lang="scss" module>
	@import "../assets/element.scss";
	.slider{
		margin-top:100px;
		text-align:center;
		img{
			width:100%;
		}
	}
	.list{
		@include list(row);
		background:#fff;
		padding-top:40px;
		padding-bottom:20px;
		justify-content:space-around;
		a{
			text-decoration:none;
			font-size:24px;
		}
		.item{
			text-align:center;
			img{
				display:inline-block;
				width: 90px;
				height:90px;
				border-radius:50%;
				overflow:hidden;
			}
			h4{
				font-siza:26px;
				margin-top:12px;
				color:#666;
			}
		}
	}
</style>