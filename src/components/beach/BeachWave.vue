<template>
	<section class="beach-wave" >
		<img src="../../assets/beach-wave.png" alt="Beach waves">
	</section>
</template>
<script>
export default {
	name:'BeachWave',
}
</script>

<style lang="scss" scoped>
	.beach-wave{
		transform:rotate(180deg);
		position: relative;
		overflow: hidden;
		background-color: #40B6D3;
	
		&::after{
			content:"";
			height:100%;
			width: 100%;
			display: block;
			position:absolute;
			top:0;
			left:0;
			//1st color is to blend with the beach section before this
			//3rd color is to blend with LevelOne
			background-image: linear-gradient(to top, rgba(#FBD38D, 0.7) 1%, 
							transparent 70%, #40B6D3);
		}
		img{
			width: 100%;
			display: block;
			position:relative;
			animation:WaveUp 3s infinite alternate linear;
		}
	}

	@keyframes WaveUp {
		from {
			top:0;
		}
		to{
			top:50px; // positive value because .beach-wave is flipped vertically
		}
	}
</style>