<template>
	<div class="calculator-page-footer bg-[#EEF5FF] pl-[14.23px] pt-[26px] pr-[16px] pb-[20px] md:px-[19.64px] md:pt-[32.97px] md:pb-[18.5px] lg:px-[33px] lg:pt-[55.6px] lg:pb-[34.65px] xl:px-[51px] xl:pt-[65px] xl:pb-[54px]">
		<div class="calculator-page-footer__scheme md:flex md:gap-[64.68px]">
			<div class="calculator-page-footer__scheme-left md:w-full">
				<div class="calculator-page-footer__title mb-[20px]">
					<h2 class="text-[16px] text-[#093078] font-bold text-center md:text-left md:text-[18px] lg:text-[29px] xl:text-[36px]">
						<span class="block">
							Нужна помощь?
						</span>
						<span class="block">
							Мы поможем! Просто свяжитесь с нами.
						</span>
					</h2>
				</div>

				<div class="calculator-page-footer__description mb-[29px]">
					<p class="text-[12px] text-[#404456] text-center max-w-[654.55px] md:text-left md:text-[10px] lg:text-[13px] xl:text-[16px]">
						Наши специалисты с радостью ответят на все ваши вопросы и дадут профессиональную консультацию по товарам.
					</p>
				</div>
			</div>

			<div class="calculator-page-footer__scheme-right md:flex-shrink-0">
				<div class="calculator-page-footer__phone mb-[7.75px]">
					<a 
						class="text-[26px] text-[#093078] font-medium text-center block md:text-[24px] lg:text-[40px] xl:text-[50px]" 
						href="tel:88008889028"
					>
						8 (800) 888-90-28
					</a>
				</div>

				<div class="calculator-page-footer__divider mb-[7.75px] lg:text-[18px] xl:text-[24px]">
					<p class="text-[12px] text-[#404456] text-center">
						или
					</p>
				</div>

				<div class="calculator-page-footer__email">
					<a 
						class="text-[18px] text-[#093078] text-center block md:text-[20px] lg:text-[24px] xl:text-[34px]" 
						href="mailto:info@example.ru"
					>
						info@example.ru
					</a>
				</div>
			</div>
		</div>
	</div>
</template>

<script>
export default {
	name: 'CalculatorPageFooter',
}
</script>
