<template>
	<div class="calculator-page-total flex items-center pl-[26px] pt-[19px] pr-[26px] pb-[20.84px] bg-[#EEF5FF] rounded-[16px] md:pl-[27px] md:pt-[34px] md:pr-[27px] md:pb-[34.84px] lg:pl-[31px] lg:pt-[28.84px] lg:pr-[31px] lg:pb-[34px] xl:pt-[36.84px] xl:pb-[41.69px]">
		<div class="calculator-page-total__icon mr-[19px]">
			<img 
				src="@/assets/icons/info.svg" 
				alt="Иконка: информация"
			/>
		</div>

		<div class="calculator-page-total__text">
			<p class="text-[24px] text-[#0F4471] font-bold">
				Итого: {{ totalPrice }}
			</p>
		</div>
	</div>
</template>

<script>
export default {
	name: 'CalculatorPageTotal',
	props: {
		totalPrice: {
			type: Number,
			default: 0,
		},
	},
}
</script>
