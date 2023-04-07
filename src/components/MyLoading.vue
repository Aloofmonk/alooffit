<template>
	<div class="loading-screen">
		<div class="nav-icon">
			<!-- <p>LOADING...</p> -->
			<h3>
				<div v-motion :initial="{opacity: 0,  x: 600 }" :enter="{ opacity: 1, x: 0 }" :delay="500" >
					
					ALOOFFIT
				</div>
				<img v-motion :initial="{opacity: 0,  x: -600 }" :enter="{ opacity: 1, x: 0 }" :delay="1000" class="stroke" src="../images/brush-stroke-grunge-transparent-background-6.png" alt="">
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
}
.nav-icon{
	font-family: 'Delicious Handrawn', cursive;
	font-weight: 600;
	font-size: 100px;
	/* animation: bounce .3s alternate infinite .8s; */
}
.loading-screen .icon {
	animation: bounce 1s infinite;
	width: 100px;
}

@keyframes bounce {
	0% {
		opacity: 0;
	}

	/* 50% {
		transform: translateY(-50px);
		border-radius: 100%;
	} */

	100% {
		opacity: 1;
	}
}
</style>



