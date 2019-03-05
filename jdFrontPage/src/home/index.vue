<template lang="html">
	<div id="home">
		<Heador></Heador>
		<Slider></Slider>
		<Novice></Novice>
		<Borrow></Borrow>
		<Finance></Finance>
		<News></News>
		<Life></Life>
		<Footer></Footer>
		<Navbar></Navbar>
	</div>
	
</template>
<script>
	import Heador from '../public/header.vue'
	import Slider from './hslider.vue'
	import Novice from './novice.vue'
	import Borrow from './borrow.vue'
	import Finance from './finance.vue'
	import News from './news.vue'
	import Life from './life.vue'
	import Footer from '../public/footer.vue'
	import Navbar from '../public/navbar.vue'
	export default{
		name:'Home',
		components:{
			Heador,Slider,Novice,Borrow,Finance,News,Life,Footer,Navbar
		}
	}

</script>
<style lang="scss" module>
@import "../assets/reset.scss"
	
</style>