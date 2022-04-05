<template>
	<section class="city-block">
		<div class="city-block__buildings">
			<Building/>
			<Building/>
		</div>
	</section>
</template>
<script>
import Building from "./Building.vue";

export default {
	name:"CityBlock",
	components:{
		Building
	}
}
</script>
<style lang="scss" scoped>
.city-block{
	height:700px;
	background-color:#9798A1;
	padding:200px 50px 0 50px;
	&__buildings{
		display:flex;
		justify-content: space-between;
	}
}
</style>