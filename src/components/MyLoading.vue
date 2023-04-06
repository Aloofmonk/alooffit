<template>
	<div class="loading-screen">
		<div class="nav-icon">
			<h3>
				ALOOFFIT
				<img class="stroke" src="../images/stroke.jpg" alt="">
			</h3>
		</div>
	</div>
</template>

<script>
export default {
	name: 'MyLoadingpage',
	methods: {}
}


</script>

<style scoped>
@import url('https://fonts.googleapis.com/css2?family=Delicious+Handrawn&family=Oswald:wght@600&family=Roboto+Mono&family=Teko&display=swap');
.loading-screen {
	display: flex;
	justify-content: center;
	padding-top: 10%;
}
.stroke{
	width: 500px;
	display: block;
	animation: bounce .5s ease-in-out;
}
.nav-icon{
	font-family: 'Delicious Handrawn', cursive;
	font-weight: 600;
	font-size: 100px;
	animation: bounce .3s ease-in-out;

}
.loading-screen .icon {
	animation: bounce 1s infinite;
	width: 100px;
}

@keyframes bounce {
	0% {
		transform: scale(0.5);
	}

	/* 50% {
		transform: translateY(-50px);
		border-radius: 100%;
	} */

	100% {
		transform: scale(1);
	}
}

@media only screen and (max-width: 500px) {

	.loading-screen {
		display: flex;
		justify-content: center;
		padding-top: 70%;
		padding-left: 70px;
		width: 100%;
		height: 100%;
	}

	.loading-screen .icon {
		animation: swing 1s infinite;
		width: 60px;
	}

	@keyframes swing {
		0% {
			transform: translateX(0px);
			background: #66fcf1;
			border-radius: 100%;
		}

		50% {
			transform: translateX(-50px);
		}

		100% {
			transform: translateX(0px);
		}
	}
}</style>



