<template>
	<div class="Nav">
		<div class="nav-icon">
			<!-- <h3 v-motion :initial="{ opacity: 0, x: 300 }" :enter="{ opacity: 1, x: 0 }" :delay="1200">
				ALOOFFIT
				<img class="stroke" src="../images/brush-stroke-grunge-transparent-background-6.png" alt="">
			</h3> -->
		</div>
		<div class="nav-links">
			<ul class="ul-links">
				<!-- <li class="li"><a href="#home">home</a></li> -->
				<li v-motion :initial="{ y: -100 }" :enter="{ y: 0 }" :delay="100" class="li"><a href="#about">About</a></li>
				<li v-motion :initial="{ y: -100 }" :enter="{ y: 0 }" :delay="200" class="li"><a href="#article">Articles</a></li>
				<li v-motion :initial="{ y: -100 }" :enter="{ y: 0 }" :delay="300" class="li"> <a href="#product">Product</a></li>
				<li v-motion :initial="{ y: -100 }" :enter="{ y: 0 }" :delay="400" class="li"><a href="#blog">Blog</a></li>
			</ul>
		</div>
		<div class="cart">
			<div v-motion :initial="{ opacity:0, x: -300 }" :enter="{ opacity: 1, x: 0 }" :delay="1200" class="search-div">
				<input class="inp" type="text" placeholder="Search...">
				<font-awesome-icon class="glass-icon" icon="magnifying-glass" />
			</div>
			
		</div>
	</div>
</template>

<script>

export default{
	name: 'MyNav'
}
</script>

<style scoped>
@import url('https://fonts.googleapis.com/css2?family=Delicious+Handrawn&family=Oswald:wght@600&family=Roboto+Mono&family=Teko&display=swap');


.Nav{
	display: flex;
	justify-content: space-between;
	padding: 20px 70px;
	margin-bottom: 42px;
	font-family: 'Roboto Mono', monospace;

}
.ul-links{
	display: flex;
	gap: 50px;
	list-style: none;
}
.inp{
	width: 100px;
	color: black;
	height: 35px;
	padding-left: 10px;
	outline: none;
	border: none;
	font-family: 'Roboto Mono', monospace;
	letter-spacing: -1.5px;
}
.li{
	background-position: right bottom;
	padding: 0 4px;
	transition: all .3s ease-in-out;
}
.li:hover {
	background: linear-gradient(to right, black 50%, white 50%);
	color: white;
	background-size: 200% 100%;
	background-position: left bottom;
	cursor: pointer;
	border-radius: 2px;
}
.li:hover a{
	color: white;
}
a{
	text-decoration: none;
	transition: all .3s ease-in-out;
	color: black;
}
.nav-icon{
	font-family: 'Delicious Handrawn', cursive;
	font-weight: 600;
}
.stroke{
	width: 70px;
	display: block;
}
.search-div{
	display: flex;
	align-items: center;
	border: 1px solid black;
	padding: 0 7px 0 0;
}
.glass-icon{
	width: 15px;
	padding: 8.5px 0;
}
</style>