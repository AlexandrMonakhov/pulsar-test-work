<template>
	<div class="calculator-page pb-[71px] md:pb-[109.5px]">
		<div class="calculator-page__title mb-[24px] px-[15px] md:px-0 md:mb-[20px] lg:mb-[30px] xl:mb-[40px]">
			<h1 class="font-medium leading-10 text-[20px] text-[#0F4471] md:text-[26px] xl:text-[34px]">Валютный калькулятор</h1>
		</div>

		<div class="calculator-page__exchange-calculator-list mb-[21.68px] md:mb-[20.84px] lg:mb-[24.4px] xl:mb-[40.05px] px-[15px] md:px-0 md:flex md:gap-[27px] md:mb-0">
			<div class="calculator-page__exchange-calculator mb-[17px] md:w-full">
				<calculator-page-exchange-calculator />
			</div>

			<div class="calculator-page__list md:w-full">
				<calculator-page-list />
			</div>
		</div>

		<div class="calculator-page__footer">
			<calculator-page-footer />
		</div>
	</div>
</template>

<script>
export default {
	name: 'CalculatorPage',
}
</script>
