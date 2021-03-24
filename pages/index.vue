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

</style>
