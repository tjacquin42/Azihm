<template>
	<div id="app"
		class="container"
	>
		<div class="timeline">
			<div v-for="item in steps"
				class="swiper-slide"
			>
				<div class="timestamp">
					<span class="date">{{ item.dateLabel }}<span /></span>
				</div>
				<div class="status">
					<span>{{ item.title }}</span>
				</div>
			</div>
		</div>
	</div>
</template>

<script>
const data = [
	{ dateLabel: '2021-01-04 18:07', title: 'Gathering Information' },
	{ dateLabel: '2021-01-04 18:07', title: 'Planning' },
	{ dateLabel: '2021-01-04 18:07', title: 'Design' },
	{ dateLabel: '2021-01-04 18:07', title: 'Content Writing and Assembly' },
	{ dateLabel: '2021-01-04 18:07', title: 'Coding' },
	{ dateLabel: '2021-01-04 18:07', title: 'Testing, Review & Launch' }
];

export default {
	data: function () {
		return {
			steps: data
		};
	},
	mounted () {
		// const swiper = new Swiper('.swiper-container', {
		// 	// pagination: '.swiper-pagination',
		// 	slidesPerView: 4,
		// 	paginationClickable: true,
		// 	grabCursor: true,
		// 	paginationClickable: true,
		// 	nextButton: '.next-slide',
		// 	prevButton: '.prev-slide'
		// });
	}
};
</script>

<style lang="scss">
// body {
//   background: #e8eeff;
// }
// #app {
//   padding: 50px 0;
// }
// .timeline {
//   margin: 50px 0;
//   list-style-type: none;
//   display: flex;
//   padding: 0;
//   text-align: center;
// }
// .timeline li {
//   transition: all 200ms ease-in;
// }
// .timestamp {
//   width: 200px;
//   margin-bottom: 20px;
//   padding: 0px 40px;
//   display: flex;
//   flex-direction: column;
//   align-items: center;
//   font-weight: 100;
// }
// .status {
//   padding: 0px 40px;
//   display: flex;
//   justify-content: center;
//   border-top: 4px solid #3e70ff;
//   position: relative;
//   transition: all 200ms ease-in ;
// }

// .status span {
//   font-weight: 600;
//   padding-top: 20px;
// }
// .status span:before {
//   content: '';
//   width: 25px;
//   height: 25px;
//   background-color: #e8eeff;
//   border-radius: 25px;
//   border: 4px solid #3e70ff;
//   position: absolute;
//   top: -15px;
//   left: 42%;
//   transition: all 200ms ease-in;
// }
// .swiper-control {
//   text-align: right;
// }

// .swiper-container {
//   width: 100%;
//   height: 250px;
//   margin: 50px 0;
//   overflow: hidden;
//   padding: 0 20px 30px 20px;
// }
// .swiper-slide {
//   width: 200px;
//   text-align: center;
//   font-size: 18px;
// }
// .swiper-slide:nth-child(2n) {
//   width: 40%;
// }
// .swiper-slide:nth-child(3n) {
//   width: 20%;
// }
</style>
