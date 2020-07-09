<template>
 	<div class="wrapper">
	   <swiper :options="swiperOption">
			<swiper-slide v-for="item of swiperList" :key="item.id">
			  <img class="swiper-img" :src=item.imgUrl />
			</swiper-slide>
			<div class="swiper-pagination"  slot="pagination"></div>
	  </swiper>
	</div>
</template>

<script>
	export default {
		name: 'HomeSwiper',
		data() {
			return {
				swiperOption: {
					pagination: ".swiper-pagination",
					loop: true
				},
				swiperList: [{
					id: '0001',
					imgUrl: 'https://imgs.qunarzz.com/sight/source/1811/f3/86173f863bef61.jpg_r_640x214_52b003ac.jpg'
				},{
					id: '0002',
					imgUrl: 'https://imgs.qunarzz.com/sight/source/1811/7e/476589267ebb41.jpg_r_640x214_bf599709.jpg'
				}]
			}
		}
	}
</script>
<style lang="stylus" scoped>
	.wrapper >>> .swiper-pagination-bullet-active
		background: #fff
	.wrapper
		overflow: hidden
		width: 100%
		height: 0
		padding-bottom: 36.64%
		background: #eee
		.swiper-img
			width: 100%
</style>