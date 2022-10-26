<template>
	<div 
		class="course-page-currency-card-skeleton w-full min-h-[242px] px-[24.13px] pt-[25.92px] pb-[38px] bg-[#F8F8F8] rounded-[16px] md:min-h-[312px] xl:min-h-[330px] placeholder placeholder_animated" 
		v-if="loading"
	/>

	<div 
		class="course-page-currency-card w-full min-h-[242px] px-[24.13px] pt-[25.92px] pb-[38px] bg-[#F8F8F8] rounded-[16px] md:min-h-[312px] xl:min-h-[330px]"
		:class="$style.CoursePageCurrencyCard"
		v-else
	>
		<div class="course-page-currency-card__icon w-[49.87px] h-[50.08px] mb-[20px] md:w-[51.87px] md:h-[52.08px] lg:w-[55.87px] lg:h-[56.08px] xl:w-[70px] xl:h-[70px] md:mb-[36px] lg:mb-[32.99px] xl:mb-[37.07px]">
			<img
				class="w-full h-full object-cover"
				src="@/assets/icons/cash.svg" 
				alt="Иконка: рука с деньгами"
			/>
		</div>

		<div class="course-page-currency-card__currency-char-code mb-[20px]">
			<p class="text-[17px] text-[#0F4471] font-bold md:text-[18px] lg:text-[20px]">{{ currency.CharCode }}</p>
		</div>

		<div class="course-page-currency-card__currency-name mb-[29px]">
			<p class="text-[14px] text-[#111111] lg:text-[15px] xl:text-[16px]">{{ currency.Name }}</p>
		</div>

		<div class="course-page-currency-card__currency-property-list">
			<ul>
				<li 
					class="text-[14px] text-[#1C1C1C] font-medium mb-[12px] lg:text-[15px] xl:text-[16px]"
					:class="$style.CoursePageCurrencyCardListItem"
				>
					Номинал: {{ currency.Nominal }}
				</li>

				<li 
					class="text-[14px] text-[#1C1C1C] font-medium lg:text-[15px] xl:text-[16px]"
					:class="$style.CoursePageCurrencyCardListItem"
				>
					Курс: {{ currency.Value }}
				</li>
			</ul>
		</div>
	</div>
</template>

<script>
export default {
	name: 'CoursePageCurrencyCard',
	props: {
		loading: {
			type: Boolean,
			default: false,
		},
		currency: {
			type: Object,
			default: null,
		},
	},
}
</script>

<style lang="scss" module>
.CoursePageCurrencyCard {
	transition: all 2s cubic-bezier(0.075, 0.82, 0.165, 1);
	cursor: pointer;

	&:hover {
		filter: drop-shadow(0px 2px 10px rgba(0, 0, 0, .15));
	}

	&List {
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
}

@media screen and (min-width: 768px) {
	.CoursePageCurrencyCard {
		&List {
			&Item {
		
			&::before {
				min-width: 8.09px;
				min-height: 8.09px;
				margin-right: 10px;
			}
		}
	}
}
}

@media screen and (min-width: 1280px) {
	.CoursePageCurrencyCard {
		&List {
			&Item {
		
				&::before {
					margin-right: 8.37px;
				}
			}
		}
	}
}

@media screen and (min-width: 1600px) {
	.CoursePageCurrencyCard {
		&List {
			&Item {
		
				&::before {
					min-width: 10px;
					min-height: 10px;
					margin-right: 10.36px;
				}
			}
		}
	}
}
</style>