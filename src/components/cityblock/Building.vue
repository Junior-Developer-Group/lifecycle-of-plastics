<template>
	<div class="city-building">
		<div class="city-building__windows">
			<div class="city-building__window"
			v-for="window in windows" :key="window">
			</div>
		</div>
		<div class="city-building__door">
			<div class="city-building__door-side"></div>
			<div class="city-building__door-side"></div>
		</div>
	</div>
</template>
<script>
export default {
	name:"Building",
	data:()=>(
		{
			windows:18
		}
	)
}
</script>
<style lang="scss" scoped>
.city-building{
	width:180px;
	height:380px;
	background-color:#C4C4C4;
	padding:15px;
	box-sizing:border-box;
	
	&__windows{
		display: grid;
		justify-content: center;
		grid-gap: 15px;
		grid-template-columns: 35px 35px 35px;
		margin-bottom:10px;
	}
	&__window{
		background-color: #215979;
		height:35px;
		position:relative;
		overflow:hidden;
		&:hover::after{
			content:"";
			height:70%;
			width:250%;
			position:absolute;
			top:100%;
			left:-150%;
			transform:rotate(25deg);
			background-color: rgba(255,255,255,0.5);
			animation:reflection 1.5s infinite forwards;
		}
	}

	&__door{
		margin:auto;
		display:flex;
		justify-content: space-between;
		width:80px;
		background-color: #737073;
		perspective: 100px;
		&-side{
			background-color: #223743;
			width:48%;
			height: 50px;
			position:relative;
			transition:transform 0.3s;
			&:nth-child(1){
				transform-origin: 0;
			}
			&:nth-child(2){
				transform-origin: 100%;
			}
			
			&::after{
				content:"";
				height:5px;
				width:5px;
				background-color: #C4C4C4;
				border-radius:50%;
				display:block;
				position:absolute;	
				top:50%;
				bottom:50%;
				margin:auto 5%;
			}

			&:nth-child(1)::after{
				right:0;
			}
		}

		&:hover &-side{
			&:nth-child(1){
				transform-origin: 0;
				transform:rotateY(-30deg);
			}
			&:nth-child(2){
				transform-origin: 100%;
				transform:rotateY(30deg);
			}
		}
	}

	@keyframes reflection{
		0%{
			opacity:0;
		}
		25%{
			opacity:1;
		}
		100%{
			top:-50%;
			left:50%;
			opacity:0;
		}
	}
}
</style>