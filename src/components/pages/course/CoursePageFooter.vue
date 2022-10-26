<template>
	<div class="course-page-footer bg-[#F8F8F8] px-[28.53px] py-[32px] rounded-[16px] md:flex items-center">
    <div class="course-page-footer__icon w-[42.47px] h-[42.4px] mb-[30px] md:mb-0 md:mr-[25px] lg:mr-[19.7px] xl:mr-[30px] md:w-[39.92px] md:h-[40.4px] lg:w-[44.92px] lg:h-[45px] xl:w-[50px] xl:h-[48.47px]">
      <img 
        class="w-full h-full object-cover"
        src="@/assets/icons/info-dark.svg" 
        alt="Иконка: информация"
      />
    </div>

    <div class="course-page-footer__phone">
      <p class="text-[16px] text-[#0F4471] font-bold md:text-[18px] lg:text-[20px]">
        Телефон: <a href="tel:88008889028">8 (800) 888-90-28</a>
      </p>
    </div>

    <div class="course-page-footer__email">
      <p class="text-[16px] text-[#0F4471] font-bold md:text-[18px] lg:text-[20px]">
        email: <a href="mailto:info@example.ru">info@example.ru</a>
      </p>
    </div>
	</div>
</template>
<script>
export default {
	name: 'CoursePageFooter',
}
</script>
