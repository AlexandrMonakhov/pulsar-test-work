<template>
	<div class="calculator-page-list bg-[#EEF5FF] border border-solid border-[#DFE1F0] rounded-[16px] pl-[15.02px] pt-[26.26px] pr-[15px] pb-[19.5px] md:pl-[15px] md:pt-[22.08px] md:pb-[17.27px] lg:pl-[24.26px] lg:pt-[32.82px] lg:pr-[24.26px] lg:pb-[33.94px] xl:pl-[30px] xl:pt-[40.59px] xl:pr-[30px] xl:pb-[40px]">
		<div class="calculator-page-list__title mb-[30px]">
			<h2 class="text-[13px] text-[#0F4471] font-medium uppercase">Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor:</h2>
		</div>

		<div class="calculator-page-list__list-photos md:flex md:justify-between md:gap-[30px] lg:items-start">
			<div class="calculator-page-list__list mb-[31px] w-full">
				<ul>
					<li
						class="mb-[20.74px] text-[#404456] text-[14px] md:text-[13px] lg:text-[14px] xl:text-[18px]"
						:class="$style.CalculatorPageListItem"
					>
						Incididunt ut labore et dolore magna aliqua
					</li>
					<li
						class="mb-[20.04px] text-[#404456] text-[14px] md:text-[13px] lg:text-[14px] xl:text-[18px]"
						:class="$style.CalculatorPageListItem"
					>
						Incididunt ut labore et
					</li>
					<li
						class="mb-[20.07px] text-[#404456] text-[14px] md:text-[13px] lg:text-[14px] xl:text-[18px]"
						:class="$style.CalculatorPageListItem"
					>
						Incididunt ut labore et dolore
					</li>
					<li
						class="mb-[20.07px] text-[#404456] text-[14px] md:text-[13px] lg:text-[14px] xl:text-[18px]"
						:class="$style.CalculatorPageListItem"
					>
						Labore et dolore
					</li>
					<li
						class="mb-[20.04px] text-[#404456] text-[14px] md:text-[13px] lg:text-[14px] xl:text-[18px]"
						:class="$style.CalculatorPageListItem"
					>
						Incididunt ut
					</li>
					<li
						class="mb-[20.04px] text-[#404456] text-[14px] md:text-[13px] lg:text-[14px] xl:text-[18px]"
						:class="$style.CalculatorPageListItem"
					>
						Incididunt ut labore et dolore
					</li>
					<li
						class="mb-[20.04px] text-[#404456] text-[14px] md:text-[13px] lg:text-[14px] xl:text-[18px]"
						:class="$style.CalculatorPageListItem"
					>
						Incididunt ut labore
					</li>
				</ul>
			</div>
			<div class="calculator-page-list__photos flex gap-[7.31px] md:flex-col md:gap-[5px] lg:flex-wrap lg:flex-row lg:w-full">
				<div class="calculator-page-list__photo overflow-hidden rounded-bl-[15px] rounded-tr-[15px] w-[69.48px] h-[46.86px] md:w-[86px] md:h-[58px] lg:w-[116.51px] lg:h-[116.51px] xl:w-[146px] xl:h-[146px] lg:rounded-none">
					<img
						class="w-full h-full object-cover"
						src="@/assets/images/img-1.jpg"
						alt="Изображение: дома под открытым небом"
					/>
				</div>
				<div class="calculator-page-list__photo overflow-hidden rounded-tl-[15px] rounded-br-[15px] w-[69.48px] h-[46.86px] md:w-[86px] md:h-[58px] lg:w-[116.51px] lg:h-[116.51px] xl:w-[146px] xl:h-[146px] lg:rounded-tr-[50px] lg:rounded-bl-none lg:rounded-br-none lg:rounded-tl-none">
					<img
						class="w-full h-full object-cover"
						src="@/assets/images/img-2.jpg"
						alt="Изображение: офис"
					/>
				</div>
				<div class="calculator-page-list__photo overflow-hidden rounded-bl-[15px] rounded-tr-[15px] w-[69.48px] h-[46.86px] md:w-[86px] md:h-[58px] md:rounded-tl-[15px] md:rounded-br-[15px] md:rounded-bl-none md:rounded-tr-none lg:w-[116.51px] lg:h-[116.51px] xl:w-[146px] xl:h-[146px] lg:rounded-tr-none lg:rounded-bl-[50px] lg:rounded-br-none lg:rounded-tl-none">
					<img
						class="w-full h-full object-cover"
						src="@/assets/images/img-3.jpg"
						alt="Изображение: торговый центр"
					/>
				</div>
				<div class="calculator-page-list__photo overflow-hidden rounded-tl-[15px] rounded-br-[15px] w-[69.48px] h-[46.86px] md:w-[86px] md:h-[58px] lg:w-[116.51px] lg:h-[116.51px] xl:w-[146px] xl:h-[146px] lg:rounded-none">
					<img
						class="w-full h-full object-cover"
						src="@/assets/images/img-4.png"
						alt="Изображение: завод"
					/>
				</div>
			</div>
		</div>
	</div>
</template>

<script>
export default {
	name: 'CalculatorPageList',
}
</script>

<style lang="scss" module>
.CalculatorPageList {
	&Item {
		display: flex;
		align-items: center;

		&::before {
			content: '';
			min-width: 7.77px;
			min-height: 7.76px;
			background-color: #ffffff;
			border: 2px solid #E02025;
			border-radius: 50%;
			margin-right: 9.59px;
		}
	}
}

@media screen and (min-width: 768px) {
	.CalculatorPageList {
		&Item {
			&::before {
				min-width: 8.09px;
				min-height: 8.09px;
				margin-right: 10px;
			}
		}
	}
}

@media screen and (min-width: 1280px) {
	.CalculatorPageList {
		&Item {
			&::before {
				margin-right: 8.37px;
			}
		}
	}
}

@media screen and (min-width: 1600px) {
	.CalculatorPageList {
		&Item {
			&::before {
				min-width: 10px;
				min-height: 10px;
				margin-right: 10.36px;
			}
		}
	}
}
</style>