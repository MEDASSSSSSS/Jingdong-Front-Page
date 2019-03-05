<template lang="html">
	<Panel title="新品推荐" :class="$style.panel">
		<section :class="$style.news">
			<div>更多尖货></div>
			<Slider :options="options" :items="items" :cname="$style.proSlider"/>
		</section>
	</Panel>
</template>
<script>
	import Panel from "../components/panel.vue"
	import Slider from "../components/slider.vue"
	export default{
		data(){
			return {
				options:{
          			slidesPerView: 3,
			        spaceBetween: 30,
			        freeMode: true,
			        
			    },
				items:[{
					href:'home',
					src:'//img13.360buyimg.com/mobilecms/s140x140_jfs/t25948/335/2359274050/92248/4d07464e/5bc854e7N53db0d18.jpg'
				},
				{
					href:'home',
					src:'//img11.360buyimg.com/mobilecms/s180x260_jfs/t1/23551/24/9258/41143/5c7cc4e1E05f7eb0e/e25047bda156a0a0.jpg'
				},
				{
					href:'home',
					src:'//img13.360buyimg.com/mobilecms/s140x140_jfs/t25948/335/2359274050/92248/4d07464e/5bc854e7N53db0d18.jpg'
				},
				{
					href:'home',
					src:'//img11.360buyimg.com/mobilecms/s180x260_jfs/t1/23551/24/9258/41143/5c7cc4e1E05f7eb0e/e25047bda156a0a0.jpg'
				}
				,]
			}
		},
		components:{
			Panel,Slider
		}
	}

</script>
<style lang="scss">
.proSlider{
	.swiper-container{
		box-sizing:border-box;
		padding:0 24px;
		.swiper-slide{
			a{
				display:inline-block;
				width:100%;
				text-align:center;
				img{
					width:100%;
					display:block;
					height:314px;
					border:1px solid #fafafa;
				}
			}
		}
	}
}
</style>
<style lang="scss" module>
 @import "../assets/element.scss";
 .panel{
 	@include panel;
 	margin-top:20px;
 	.news{
		padding-bottom:40px;
		position:relative;
		>div{
			position:absolute;
			right:30px;
			top:-70px;
			color:#999;
			font-size:28px;
		}
 	}
 }
	
</style>