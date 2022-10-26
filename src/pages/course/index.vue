<template>
	<div class="course-page pb-[98px] md:pb-[44px] lg:pb-[108px] xl:pb-[92px]">
		<div class="course-pagee__title mb-[24px] px-[15px] md:px-0 md:mb-[20px] lg:mb-[30px] xl:mb-[40px]">
			<h1 class="font-medium leading-10 text-[20px] text-[#0F4471] md:text-[26px] xl:text-[34px]">Курс рубля</h1>
		</div>

		<div class="course-page__currency-cards flex flex-wrap gap-[20px] justify-between px-[15px] mb-[16px] md:px-0 md:mb-[30px] lg:mb-[48px] xl:mb-[30px]">
			<div 
				class="course-page__currency-card w-full md:w-[48%] lg:w-[31%]"
				v-for="(currency) in currencies"
				:key="currency.ID"
			>
				<course-page-currency-card 
					:loading="loading" 
					:currency="currency"
				/>
			</div>
		</div>

		<div class="course-page__footer px-[15px] md:px-0">
			<course-page-footer />
		</div>
	</div>
</template>

<script>
import axios from "axios";

export default {
	name: 'CoursePage',
	data() {
		return {
			loading: false,
			currencies: null,
		}
	},
	computed: {
		currenciesArray() {
			if (!this.currencies) return;

			return Object.entries(this.currencies);
		},
	},
	async mounted() {
		this.loading = true;

		this.currencies = await axios
			.get('https://www.cbr-xml-daily.ru/daily_json.js')
			.then(response => response.data.Valute);

		this.loading = false;
	},
}
</script>
