<template>
	<view class="content">
		<view class="swiper-dot">
			<swiper class="swiper-box" :indicator-dots="indicatorDots" :autoplay="autoplay" :interval="interval" :duration="duration" :current='current' >
				<swiper-item v-for="(item ,index) in info" :key="index">
					<image :src="item.url" mode="scaleToFill" class="swiper-img">
						
					</image>
				</swiper-item>
			</swiper>
		</view>
		首页
	</view>
</template>

<script>
	export default {
		data() {
			return {
				info: [{
					url: '../../static/img/swiper1.jpg'
				}, {
					url: '../../static/img/swiper2.jpg'
				}, {
					url: '../../static/img/swiper3.jpg'
				}],
				current: 0,
				autoplay: true,// 控住是否自动切换
				indicatorDots: true,// 是否显示面板指示点
				interval: 3000, // 自动切换的时间间隔
				duration: 500 // 滑动动画的时长
			}
		},
		onLoad() {

		},
		mounted() {
		},
		methods: {
			

		}
	}
</script>

<style lang="scss">

.swiper-img {
	width: 100%;
	height: 300rpx;
}
</style>
