<template>
	<div class="beach-pathway" role="group">
		<button v-for="step in numSteps" :key="step"
		:class="['beach-pathway__step', step == selectedStep? 'selected':'']" 
		@click="handleStepClick(step)">
		</button>
		<p aria-live="polite">
			<strong v-if="step == selectedStep">
				Hooray! You found the surprise step. Congrats...
			</strong>
		</p>
	</div>
</template>
<script>
export default {
	name:"Pathway",
	mounted(){
		this.updateSurpriseStep();
	},
	data:()=>(
		{
			numSteps:16,
			surpriseStep:-1,
			selectedStep:-1
		}
	),
	methods:{
		updateSurpriseStep(){
			const prevSurpriseStep = this.surpriseStep

			const min = 0
			const max = this.numSteps
			// Ensure no similar random number as previous
			while(prevSurpriseStep == this.surpriseStep){
				this.surpriseStep = Math.floor(Math.random() * (max - min) + min)
			}
		},
		/**
		 * Handle click event for pathway step
		 * Trigger a fade-in logo
		 */
		handleStepClick(step){
			if(step === this.surpriseStep){
				this.selectedStep = step
				this.updateSurpriseStep()
			}
		}
	}
}
</script>
<style lang="scss">
.beach-pathway{
	max-width: fit-content;
	&__step{
		position: relative;
		background-color: #AF7878;
		display: block;
		height:20px;
		width:70px;
		border:1px solid black;
		transition:transform 0.3s;
		&:hover{
			transform:scale(1.2);
			z-index: 1;
		}

		&.selected{
			animation:switchColor 0.5s 1 alternate;
			&::after{
				content:"";
				height:50px;
				width:50px;
				background-image:url("https://junior-developer-group.com/assets/images/website-images/logo-with-background.png");
				background-size: contain;
				background-position: center;
				background-repeat: no-repeat;
				position:absolute;
				top:0;
				left:100%;
				animation:fadeUp 1s 1 forwards;
			}
		}
	}

	@keyframes switchColor{
		0%{
			background-color: #AF7878;
		}
		100%{
			background-color: yellow;
		}
	}

	@keyframes fadeUp{
		0%{
			top:0;
			opacity:0;
		}
		75%{
			top:-55px;
			opacity:1;
		}
		100%{
			top:-80px;
			opacity:0;
		}
	}
}
</style>