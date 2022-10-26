<template>
	<div class="navigation flex">
		<div class="navigation__link mr-[29.78px] md:mr-[35px] lg:mr-[30.78px] xl:mr-[31px]">
			<nuxt-link
				to="/calculator"
				exact
			>
				Калькулятор
			</nuxt-link>
		</div>

		<div class="navigation__link">
			<nuxt-link
				to="/course"
				exact
			>
				Курс рубля
			</nuxt-link>
		</div>
	</div>
</template>

<script>
export default {
	name: "Navigation",
}
</script>