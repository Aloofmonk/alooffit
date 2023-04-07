<template>
	<div id="product" class="product">
		<div v-motion :initial="{ opacity: 0, y: 100 }" :visibleOnce="{ opacity: 1, y: 0 }" :delay="400" class="box">
			<h2>NIKE</h2>
			<img src="../images/nike.png" alt="">
		</div>
		<div v-motion :initial="{ opacity: 0, y: 100 }" :visibleOnce="{ opacity: 1, y: 0 }" :delay="500" class="box">
			<h2>ADIDAS</h2>
			<img src="../images/addshoe.png" alt="">
		</div>
		<div v-motion :initial="{ opacity: 0, y: 100 }" :visibleOnce="{ opacity: 1, y: 0 }" :delay="600" class="box">
			<h2>VANS</h2>
			<img src="../images/vansshoe.png" alt="">
		</div>
		<div v-motion :initial="{ opacity: 0, y: 100 }" :visibleOnce="{ opacity: 1, y: 0 }" :delay="700" class=" last box">
			<h2>CONVERSE</h2>
			<img src="../images/converseshoe.webp" alt="">
		</div>
	</div>
</template>

<script>

	export default{
		name: 'MyProduct',
		data(){
			return{
				show: 'img-no-show'
			}
		}
	}
</script>

<style scoped>
@import url('https://fonts.googleapis.com/css2?family=Oswald:wght@600&family=Roboto+Mono&family=Teko&display=swap');

.product{
	display: flex;
	flex-direction: column;
	background: black;
	color: rgba(117, 117, 117, 1);
	justify-content: center;
	padding: 56px 0;
	padding-left: 5%;
}
.box{
	display: flex;
	justify-content: space-between;
	width: 95%;
	border-bottom: 1px solid rgba(117, 117, 117, 1);
	font-family: 'Teko', sans-serif;
	font-size: 55px;
	padding-top: 10px;
	transition: all 0.3s ease-out;
	cursor: pointer;
}
.box:hover{
	color: white;
}
.box:hover img{
	width: 150px;
	opacity: 1;
}
img{
	opacity: 0;
	width: 150px;
	transition: all 0.2s ease-out;
}
.last{
	padding-top: 0px;
}
</style>