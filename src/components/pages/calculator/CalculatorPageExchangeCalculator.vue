<template>
	<div class="calculator-page-exchange-calculator">
		<div class="calculator-page-exchange-calculator__currency flex flex-col mb-[21px] md:mb-[31px] lg:mb-[30.05px]">
			<label class="mb-[14px] lg:mb-[15.14px] text-[#2C3A4B] text-[14px] xl:text-[16px] font-medium">
				Валюта 1
			</label>

			<input 
				class="pl-[20px] pt-[20px] pr-[20px] pb-[18px] lg:pb-[21px] border border-solid border-[#DFDFDF] rounded-[5px] placeholder-[#A0A3BD]"
				:class="errorClassName" 
				type="text" 
				placeholder="Введите название или код"
				v-model="firstCurrency"
				@input="convertCurrency"
			/>
		</div>

		<div class="calculator-page-exchange-calculator__currency flex flex-col mb-[19px] md:mb-[33px] lg:mb-[30px]">
			<label class="mb-[12px] lg:mb-[15.09px] text-[#2C3A4B] text-[14px] xl:text-[16px] font-medium">
				Валюта 2
			</label>

			<input 
				class="pl-[20px] pt-[20px] pr-[20px] pb-[18px] lg:pb-[21px] border border-solid border-[#DFDFDF] rounded-[5px] placeholder-[#A0A3BD]"
				:class="errorClassName" 
				type="text" 
				placeholder="Введите название или код"
				v-model="secondCurrency"
				@input="convertCurrency"
			/>
		</div>

		<div class="calculator-page-exchange-calculator__quantity flex flex-col mb-[19px] md:mb-[23px] lg:mb-[20px] xl:mb-[31px]">
			<label class="mb-[11px] lg:mb-[15.14px] text-[#2C3A4B] text-[14px] xl:text-[16px] font-medium">
				Количество
			</label>

			<input 
				class="pl-[20px] pt-[18px] pr-[20px] pb-[19px] lg:pt-[20.32px] lg:pb-[20.61px] border border-solid border-[#DFDFDF] rounded-[5px] placeholder-[#A0A3BD]" 
				type="number" 
				placeholder="Введите число"
				v-model="quantity"
				@input="convertCurrency"
			/>
		</div>

		<div class="calculator-page-exchange-calculator__total">
			<calculator-page-total :total-price="totalPrice" />
		</div>
	</div>
</template>

<script>
export default {
	name: 'CalculatorPageExchangeCalculator',
	props: {
		currencies: {
			type: Object,
			default: null,
		},
	},
	data() {
		return {
			firstCurrency: 'AUD',
			secondCurrency: 'AZN',
			quantity: 10,
			totalPrice: 0,
			exchangeError: false,
		}
	},
	computed: {
		errorClassName() {
			return this.exchangeError 
				? 'border-[#E02025]' 
				: '';
		},
	},
	mounted() {
		this.convertCurrency();
	},
	methods: {
		convertCurrency() {
			this.checkCorrectnessCurrencies();
			this.currenciesCharToUpperCase();

			const exchangeRate = +(this.currencies[this.firstCurrency]?.Value / this.currencies[this.secondCurrency]?.Value).toFixed(2);

			this.totalPrice = this.quantity * exchangeRate;
		},
		checkCorrectnessCurrencies() {
			if (
				!this.currencies[this.firstCurrency] 
				|| !this.currencies[this.secondCurrency]
			) {
				this.exchangeError = true;

				return;
			}

			this.exchangeError = false;
		},
		currenciesCharToUpperCase() {
			this.firstCurrency = this.firstCurrency.toUpperCase();
			this.secondCurrency = this.secondCurrency.toUpperCase();
		},
	},
}
</script>
