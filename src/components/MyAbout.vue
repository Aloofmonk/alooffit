<template>
	<div class="About" id="about">

		<p v-motion :initial="{ opacity: 0, }" :visibleOnce="{ opacity: 1, }" :delay="600">
			ALOOFFIT culture is a subgenre of grungewears culture - A clothing style that emerged from Aberdeen, Washington, United States. Most notable style of the rock band Nirvana's front man, Kurt Cobain. <br> <br> <span v-motion :initial="{ opacity: 0, }" :visibleOnce="{ opacity: 1, }" :delay="900">It then became the go to fashion choice of Skateboarders and persons with associated lifestyles. ALOOFFIT generally refers to a person who is devoted to acquiring fashionablly unique items, especially clothing and shoes.</span> <br> <span v-motion :initial="{ opacity: 0, }" :visibleOnce="{ opacity: 1, }" :delay="1100">To satisfy your fashion needs, ALOOFFIT is here for you! The place with dozens of high-qualtity footwears. Pristin items live here! From the Nirvana era to new school skateboarders, We've got you covered.</span> 
		</p>
	</div>
</template>

<script>
 export default{
	name: 'MyAbout'
 }

</script>

<style scoped>
.About{
	padding: 155px 0;
	display: flex;
	background: black;
	color: white;
	justify-content: center;
	align-items: center;
}
p{
	text-align: left;
	width: 45%;
	line-height: 1.5;
	font-family: 'Roboto Mono', monospace;
	letter-spacing: 1.5px;
}
span{
	display: block;
}
</style>