<template>
	<section class="beach">
		<div class="beach-land">
			<Pathway/>
		</div>
		<Wave/>
	</section>
</template>
<script>
import Pathway from "./Pathway.vue";
import Wave from "./Wave.vue";

export default {
	name:"Beach",
	components:{
		Pathway,
		Wave
	}
}
</script>
<style lang="scss" scoped>
.beach{
	position:relative;
	&-land{
		background-color:#FBD38D;
		height:500px;
	}
	&-pathway{
		position:absolute;
		top:0;
		left:0;
		right:0;
		margin:auto;
	}
}
</style>