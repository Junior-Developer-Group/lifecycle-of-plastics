<template>
    <section>
		<aside>
			<img src="../../assets/plastic-toothbrush.png" :alt="item.alt_text">
		</aside>
		<aside>
			<p v-if="shouldShowText">
                The {{ item.name}} will disolve in {{ item.time_to_dissolve }}
			</p>
			<button @click="showMeTheText" 
			:class="{'active' : shouldShowText}"> {{ item.button_text }} </button>
		</aside>
	</section>
</template>

<script>
export default {
    name: 'LevelThree',
	data(){
		return {
			item:{
				name:'Plastic Toothbrush',
				time_to_dissolve:'500 years',
				alt_text:'plastic toothbrush',
				button_text:'Reveal time to dissolve'
			},
			shouldShowText: false
		}
	},
	methods:{
		showMeTheText(){
			this.shouldShowText = !this.shouldShowText

			this.item.button_text = this.shouldShowText
									? 'Hide button text'
									: 'Reveal time to dissolve'
		}
	}
}
</script>

<style lang="scss" scoped>
section {
	height: 500px;
	background: #40B6D3;

	display: flex;
	justify-content: center;
	align-items: center;

	aside {
		img {
			height: 80px;
			margin-right: 50px;
		}

		button {
			border: none;
			padding: 5px 10px;
			background: white;
			color: darkslategrey;
		}

		button.active {
			background-color: grey;
			color: white;
		}
	}
}
</style>