<template lang="html">
	<Panel title='生活服务' :cname='$style.life'>
		<section :class='$style.content'>
			<div v-for="item in items" :key="item.title">
				<router-link :to="{name:'home'}">
					<img :src="item.src" :alt="item.title">
					<p>{{item.title}}</p>
					<p :class="[$style.update, item.updata?$style.active:'']">{{item.update}}</p>
				</router-link>
			</div>
		</section>
	</Panel>
</template>
<script>
	import Panel from '../components/panel.vue'
	export default{
		data(){
			return{
				items:[{
					title:'惠加油',
					src:'//misc.360buyimg.com/mtd/pc/common/img/no_login.jpg',
					update:'',
				},
				{
					title:'小白信用',
					src:'//misc.360buyimg.com/mtd/pc/common/img/no_login.jpg',
					update:'全新升级',
				},
				{
					title:'信用卡办理',
					src:'//misc.360buyimg.com/mtd/pc/common/img/no_login.jpg',
					update:'',
				},
				{
					title:'卡转让',
					src:'//misc.360buyimg.com/mtd/pc/common/img/no_login.jpg',
					update:'',
				},
				{
					title:'定期还款',
					src:'//misc.360buyimg.com/mtd/pc/common/img/no_login.jpg',
					update:'',
				},]
			}
		},
		components:{
			Panel,
		}
	}

</script>
<style lang="scss" module>
.life{
	margin-top:20px;
	@import "../assets/element.scss";
	.content{
		@include list(row);
		justify-content:space-around;
		background:#fff;
		padding-bottom:20px;
		div{
			width:20%;
			a{
				display:inline-block;
				text-decoration:none;
				color:#333;
				font-size:26px;
				text-align:center;
				width:100%;
				img{
					width:100px;
					height:100px;
					border-radius:50%;
				}
				p{
					box-sizing:border-box;
					padding:4px 5px;
					width:100%;
					white-space:nowrap;
					text-overflow:ellipsis;
					overflow:hidden;
				}
				.update{
					color:#ff801a;
					font-size:20px;
				}
			}
		}
	}
}
	
	
</style>