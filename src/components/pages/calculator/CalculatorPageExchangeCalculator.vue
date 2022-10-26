<template>
	<div class="calculator-page-exchange-calculator">
		<div class="calculator-page-exchange-calculator__currency flex flex-col mb-[21px] md:mb-[31px] lg:mb-[30.05px]">
			<label class="mb-[14px] lg:mb-[15.14px] text-[#2C3A4B] text-[14px] xl:text-[16px] font-medium">
				Валюта 1
			</label>

			<input 
				class="pl-[20px] pt-[20px] pr-[20px] pb-[18px] lg:pb-[21px] border border-solid border-[#DFDFDF] rounded-[5px] placeholder-[#A0A3BD]" 
				type="text" 
				placeholder="Введите название или код" 
			/>
		</div>

		<div class="calculator-page-exchange-calculator__currency flex flex-col mb-[19px] md:mb-[33px] lg:mb-[30px]">
			<label class="mb-[12px] lg:mb-[15.09px] text-[#2C3A4B] text-[14px] xl:text-[16px] font-medium">
				Валюта 2
			</label>

			<input 
				class="pl-[20px] pt-[20px] pr-[20px] pb-[18px] lg:pb-[21px] border border-solid border-[#DFDFDF] rounded-[5px] placeholder-[#A0A3BD]" 
				type="text" 
				placeholder="Введите название или код" 
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
		totalPrice: {
			type: Number,
			default: 0,
		},
	},
}
</script>
