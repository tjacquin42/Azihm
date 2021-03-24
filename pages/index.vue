<template>
	<div justify="center"
		align="center"
	>
		<div>
			<v-data-table
				:headers="headers"
				:items="desserts"
				class="elevation-1"
			>
				<template #item.calories="{ item }">
					<v-chip
						:color="getColor(item.calories)"
						dark
					>
						{{ item.calories }}
					</v-chip>
				</template>
			</v-data-table>
		</div>

		<div>
			<timeline />
		</div>
	</div>
</template>

<script>
import Timeline from '~/components/Timeline';

const data = [
	{ dateLabel: 'January 2017', title: 'Gathering Information' },
	{ dateLabel: 'February 2017', title: 'Planning' },
	{ dateLabel: 'March 2017', title: 'Design' },
	{ dateLabel: 'April 2017', title: 'Content Writing and Assembly' },
	{ dateLabel: 'May 2017', title: 'Coding' },
	{ dateLabel: 'June 2017', title: 'Testing, Review & Launch' },
	{ dateLabel: 'July 2017', title: 'Maintenance' }
];

export default {
	components: {
		Timeline
	},
	data () {
		return {
			headers: [
				{
					text: 'N° NOTE',
					align: 'start',
					sortable: false,
					value: 'name'
				},
				{ text: 'SALES ORG', value: 'sales' },
				{ text: 'DOCUMENT TYPE', value: 'docType' },
				{ text: 'CUSTOMER NAME', value: 'customer' },
				{ text: 'INDUSTRY', value: 'industry' },
				{ text: 'DATE', value: 'date' },
				{ text: 'REQUESTOR', value: 'requestor' },
				{ text: 'AMOUNT', value: 'amount' },
				{ text: 'APPROVER', value: 'approver' },
				{ text: 'STATUS', value: 'status' }

			],
			desserts: [
				{
					name: '111',
					sales: 'PS FRANCE',
					docType: 'Litigation Returns',
					customer: 'APTGOSS Menuisiers indus',
					industry: 'SGGSIndustry',
					date: '8/6/2020',
					requestor: 'Jean Dupont',
					amount: '10,096,19 EUR',
					approver: 'Olivier Duboit',
					status: 'down'
				},
				{
					name: '111',
					sales: 'PS FRANCE',
					docType: 'Litigation Returns',
					customer: 'APTGOSS Menuisiers indus',
					industry: 'SGGSIndustry',
					date: '8/6/2020',
					requestor: 'Jean Dupont',
					amount: '10,096,19 EUR',
					approver: 'Olivier Duboit',
					status: 'down'
				},
				{
					name: '111',
					sales: 'PS FRANCE',
					docType: 'Litigation Returns',
					customer: 'APTGOSS Menuisiers indus',
					industry: 'SGGSIndustry',
					date: '8/6/2020',
					requestor: 'Jean Dupont',
					amount: '10,096,19 EUR',
					approver: 'Olivier Duboit',
					status: 'down'
				}
			],
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
	},

	methods: {
		getColor (calories) {
			if (calories > 400) return 'red';
			else if (calories > 200) return 'orange';
			else return 'green';
		}
	}
};
</script>

<style lang="scss">
body {
  background: #e8eeff;
}
#app {
  padding: 50px 0;
}
.timeline {
  margin: 50px 0;
  list-style-type: none;
  display: flex;
  padding: 0;
  text-align: center;
}
.timeline li {
  transition: all 200ms ease-in;
}
.timestamp {
  width: 200px;
  margin-bottom: 20px;
  padding: 0px 40px;
  display: flex;
  flex-direction: column;
  align-items: center;
  font-weight: 100;
}
.status {
  padding: 0px 40px;
  display: flex;
  justify-content: center;
  border-top: 4px solid #3e70ff;
  position: relative;
  transition: all 200ms ease-in ;
}

.status span {
  font-weight: 600;
  padding-top: 20px;
}
.status span:before {
  content: '';
  width: 25px;
  height: 25px;
  background-color: #e8eeff;
  border-radius: 25px;
  border: 4px solid #3e70ff;
  position: absolute;
  top: -15px;
  left: 42%;
  transition: all 200ms ease-in;
}
.swiper-control {
  text-align: right;
}

.swiper-container {
  width: 100%;
  height: 250px;
  margin: 50px 0;
  overflow: hidden;
  padding: 0 20px 30px 20px;
}
.swiper-slide {
  width: 200px;
  text-align: center;
  font-size: 18px;
}
.swiper-slide:nth-child(2n) {
  width: 40%;
}
.swiper-slide:nth-child(3n) {
  width: 20%;
}
</style>
