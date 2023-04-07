<template>
	<div class="contact" id="contact">

		<div class="black-banner">
			<img v-motion :initial="{ opacity: 0, }" :visibleOnce="{ opacity: 1, }" :delay="400" src="../images/brush-stroke-grunge-transparent-background-6.png" alt="">
		</div>
		<div v-motion :initial="{ opacity: 0 }" :visibleOnce="{ opacity: 1 }" :delay="600" class="middle-cont">
			<div class="sub-flex">
	
				<div class="one">
					<p>ABOUT US</p>
					<p>FAQ</p>
					<p>CONTACT US</p>
					<p>PRODUCTS</p>
					<p>CAREER</p>
				</div>
				<div class="two">
					<p>PRIVACY POLICY</p>
					<p>REFUND POLICY</p>
					<p>TERMS OF SERVICE</p>
					<p>CUSTOMER CARE</p>
				</div>
				<div class="three">
					<p>HOW TO ORDER</p>
					<p>HOW TO REFUND</p>
					<p>TRACK YOUR ORDER</p>
				</div>
			</div>
			<div class="sub-contact">
				<h1>JOIN OUR COMMUNITY</h1>
				<div class="inp">
					<input type="text" name="" id="" placeholder="ENTER YOUR EMAIL">
				</div>
			</div>
		</div>
		<div class="last-flex">
			<div class="copy-write">
				&copy;2023ALOOFFIT, All right reserved
			</div>
			<div class="socials">
				<p>INSTAGRAM</p>
				<p>TWITTER</p>
				<p>FACEBOOK</p>
				<p>LINKEDIN</p>
			</div>
		</div>
	</div>
	
</template>

<script>
	export default{
		name: 'MyContact'
	}
</script>

<style scoped>
@import url('https://fonts.googleapis.com/css2?family=Delicious+Handrawn&family=Oswald:wght@200;600&family=Roboto+Mono&family=Teko&display=swap');
.contact{
	/* height: 100vh; */
	padding-top: 30px;
}
.black-banner{
	height: 348px;
	background: black;
	padding-left: 30px;
	padding-top: 80px;
}
img{
	width: 100%;
	filter: invert(100%);
}
.middle-cont{
	margin-top: 50px;
	margin-left: 75px;
	width: 90%;
	display: flex;
	justify-content: space-between;
	align-items: center;
	height: 40%;
	border-bottom: 1px solid black;
	padding-bottom: 10px;
}
.last-flex{
	margin-left: 75px;
	width: 90%;
	display: flex;
	justify-content: space-between;
	font-family: 'Roboto Mono', monospace;
	word-spacing: -8px;
	align-content: center;
	padding-top: 25px;
}
.socials{
	display: flex;
}
.socials > p{
	padding-left: 25px;
}
.sub-flex{
	display: flex;
}
p{
	padding-bottom: 20px;
	font-family: 'Roboto Mono', monospace;
	word-spacing: -5px;
}
.two{
	margin-left: 55px;
}
.three{
	margin-left: 55px;
}
.inp{
	display: inline-block;
	border: 1px solid black;
	padding: 0px 60px;
	padding-left: 20px;

}
input{
	outline: none;
	border: none;
	text-align: left;
	width: 200px;
	height: 50px;
}
h1{
	font-family: 'Teko', sans-serif;
}
.sub-contact{
	margin-bottom: 70px;
}
/* .stroke{
	width: 50px;
	display: block;
	animation: bounce .5s ease-in-out;
}
.nav-icon{
	color: white;
	font-family: 'Delicious Handrawn', cursive;
	font-weight: 600;
	font-size: 60px;
	animation: bounce .3s ease-in-out;
} */
</style>