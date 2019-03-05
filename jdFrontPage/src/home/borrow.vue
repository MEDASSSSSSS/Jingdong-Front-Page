<template lang="html">
	<Panel title="极速借贷" :class="$style.borrow">
		<section :class="$style.content">
			<router-link :to="{name:'home',params:{}}">
				<img src="//misc.360buyimg.com/mtd/pc/common/img/no_login.jpg" alt="">
			</router-link>
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
.borrow{
	@include panel($margin:20px 0);
	.content{
		padding-bottom:40px;
		img{
			display:block;
			margin:20px auto;
		}
	}

}
</style>