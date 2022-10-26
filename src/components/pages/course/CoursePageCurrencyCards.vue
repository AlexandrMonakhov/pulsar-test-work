<template>
  <div class="course-page__currency-cards flex flex-wrap gap-[20px] justify-between px-[15px] mb-[16px] md:px-0 md:mb-[30px] lg:mb-[48px] xl:mb-[30px]">
    
    
    <div class="course-page__currency-card w-full md:w-[48%] lg:w-[31%]">
      <course-page-currency-card />
    </div>

    <div class="course-page__currency-card w-full md:w-[48%] lg:w-[31%]">
      <course-page-currency-card />
    </div>

    <div class="course-page__currency-card w-full md:w-[48%] lg:w-[31%]">
      <course-page-currency-card />
    </div>
  </div>
</template>

<script>
export default {
	name: 'CoursePageCurrencyCards',
  props: {
		loading: {
			type: Boolean,
			default: false,
		},
  }
}
</script>