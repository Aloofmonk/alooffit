<template>
	<div class="article" id="article">
		<div class="top-div">
			<div class="text">NEW <span v-motion :initial="{ opacity: 0, }" :visibleOnce="{ opacity: 1, }" :delay="300">ARTICLE</span></div>
			<div v-motion :initial="{ opacity: 0 }" :visibleOnce="{ opacity: 1 }" :delay="500" class="button-border">
				<div v-motion :initial="{ opacity: 0, x: -100 }" :visibleOnce="{ opacity: 1, x: 0 }" :delay="800" @click="more = !more, horizontalScrollUsed = !horizontalScrollUsed" class="button">
					{{more === true ? 'RESTORE' : 'VIEW MORE'}}
				</div>
			</div>
		</div>
		<font-awesome-icon :class="[horizontalScrollUsed === true ? 'font-icon-none': 'font-icon']" icon="arrow-right" shake />
		<div v-motion :initial="{ opacity: 0, x: -200 }" :visibleOnce="{ opacity: 1, x: 0 }" :delay="800" @scroll="onScroll" class="bottom-div">
			<div :class="[more === true ? 'view-none' : 'card']">
				<div class="top-card">
					<div class="icons"><img class="icon" src="../images/vans.png" alt=""></div>
					<div class="amount">$65.00</div>
				</div>
				<div class="mid-card">
					<img src="../images/nike.png" alt="">
				</div>
				<div class="bottom-card">
					<div class="header">CLASSIC SLIP ON</div>
					<div class="paragraph">First introduced in 1977, the Vans #98</div>
				</div>
			</div>
			<div :class="[more === true ? 'view-none' : 'card']">
				<div class="top-card">
					<div class="icons"><img class="icon" src="../images/adidas_318-565831.avif" alt=""></div>
					<div class="amount">$115.00</div>
				</div>
				<div class="mid-card">
					<img src="../images/addidasshoe.jpg" alt="">
				</div>
				<div class="bottom-card">
					<div class="header">RAIN FENDER</div>
					<div class="paragraph">First introduced in 1177, the Adidas #32</div>
				</div>
			</div>
			<div :class="[more === true ? 'view-none' : 'card']">
				<div class="top-card">
					<div class="icons"><img class="icon" src="../images/puma.png" alt=""></div>
					<div class="amount">$361.00</div>
				</div>
				<div class="mid-card">
					<img src="../images/converseshoe.webp" alt="">
				</div>
				<div class="bottom-card">
					<div class="header">HIGH TILT</div>
					<div class="paragraph"> 2077, the Converse #118</div>
				</div>
			</div>
			<div :class="[more === true ? 'view-none' : 'card']">
				<div class="top-card">
					<div class="icons"><img class="icon" src="../images/vans.png" alt=""></div>
					<div class="amount">$605.00</div>
				</div>
				<div class="mid-card">
					<img src="../images/vansshoe.png" alt="">
				</div>
				<div class="bottom-card">
					<div class="header">GUIL RELEASE</div>
					<div class="paragraph">Sapphire 607, the Vans #626</div>
				</div>
			</div>
			<div :class="[more === true ? 'view-none' : 'card']">
				<div class="top-card">
					<div class="icons"><img class="icon" src="../images/nike_318-565950.webp" alt=""></div>
					<div class="amount">$94.00</div>
				</div>
				<div class="mid-card">
					<img src="../images/addidasshoe.jpg" alt="">
				</div>
				<div class="bottom-card">
					<div class="header">CLASSIC SLIP ON</div>
					<div class="paragraph">First introduced in 1977, the Vans #98</div>
				</div>
			</div>
			<div :class="[more === true ? 'view-none' : 'card']">
				<div class="top-card">
					<div class="icons"><img class="icon" src="../images/adidas_318-565831.avif" alt=""></div>
					<div class="amount">$144.00</div>
				</div>
				<div class="mid-card">
					<img src="../images/addshoe.png" alt="">
				</div>
				<div class="bottom-card">
					<div class="header">GALACTIC PRINCIPLE</div>
					<div class="paragraph">Kryon Asta 847, the Adidas Supreme</div>
				</div>
			</div>
			<div class="card">
				<div class="top-card">
					<div class="icons"><img class="icon" src="../images/vans.png" alt=""></div>
					<div class="amount">$65.00</div>
				</div>
				<div class="mid-card">
					<img src="../images/nike.png" alt="">
				</div>
				<div class="bottom-card">
					<div class="header">CLASSIC SLIP ON</div>
					<div class="paragraph">First introduced in 1977, the Vans #98</div>
				</div>
			</div>
			<div class="card">
				<div class="top-card">
					<div class="icons"><img class="icon" src="../images/vans.png" alt=""></div>
					<div class="amount">$65.00</div>
				</div>
				<div class="mid-card">
					<img src="../images/nike.png" alt="">
				</div>
				<div class="bottom-card">
					<div class="header">CLASSIC SLIP ON</div>
					<div class="paragraph">First introduced in 1977, the Vans #98</div>
				</div>
			</div>
			<div class="card">
				<div class="top-card">
					<div class="icons"><img class="icon" src="../images/vans.png" alt=""></div>
					<div class="amount">$65.00</div>
				</div>
				<div class="mid-card">
					<img src="../images/nike.png" alt="">
				</div>
				<div class="bottom-card">
					<div class="header">CLASSIC SLIP ON</div>
					<div class="paragraph">First introduced in 1977, the Vans #98</div>
				</div>
			</div>
			<div class="card">
				<div class="top-card">
					<div class="icons"><img class="icon" src="../images/vans.png" alt=""></div>
					<div class="amount">$65.00</div>
				</div>
				<div class="mid-card">
					<img src="../images/nike.png" alt="">
				</div>
				<div class="bottom-card">
					<div class="header">CLASSIC SLIP ON</div>
					<div class="paragraph">First introduced in 1977, the Vans #98</div>
				</div>
			</div>
		</div>
	</div>
</template>

<script>
	export default{
		name: 'MyNewArticle',
		data(){
			return{
				horizontalScrollUsed: false,
				more: false
			}
		},
		methods: {
		onScroll(event) {
			if (event.target.scrollLeft > 0) {
				this.horizontalScrollUsed = true;
			} else{
				this.horizontalScrollUsed = false
			}
		}
	}

		
}

</script>

<style scoped>
@import url('https://fonts.googleapis.com/css2?family=Delicious+Handrawn&family=Oswald:wght@200;600&family=Roboto+Mono&family=Teko&display=swap');

.article{
	
	/* height: 100%; */
	padding: 80px 0;
	margin-bottom: 50px;
}
.top-div{
	display: flex;
	justify-content: space-between;
	height: 30%;
	border-bottom: 2px solid #807f7f;
	align-items: center;
	padding: 0 55px;
}
.bottom-div{
	display: flex;
	align-items: center;
	padding: 60px 0 0 20px;
	overflow-y: auto;
    white-space: nowrap;
	margin: 0px 30px;
}

.bottom-div::-webkit-scrollbar {
  height: 0;
  width: 0;
  background: transparent;
}
.text{
	font-family: 'Teko', sans-serif;
	font-size: 80px;
}
img{
	width: 200px;
	height: 200px;
	
}
.icon{
	width: 25px;
	height: 30px;
}
.amount{
	padding-top: 7px;
	font-family: 'Teko', sans-serif;
	font-weight: bold;
}
.mid-card{
	border-left: 2px solid #807f7f;
	border-right: 2px solid #807f7f;
	background: rgb(241, 238, 238);
}
.card{
	display: inline-block;
	margin-right: 20px;
	opacity: 1;
	transition: all .5s ease-out;
}
.bottom-card{
	border: 2px solid #807f7f;
	padding: 6px;
	font-family: 'Teko', sans-serif;
	
}
.header{
	font-weight: bold;
}
.paragraph{
	font-weight: lighter;
	width: -20px;
	color: rgb(163, 161, 161);
}
.top-card{
	display: flex;
	justify-content: space-between;
	border: 2px solid #807f7f;
	padding: 0px 7px;
	background: #cacaca;
}
.button{
	position: relative;
	right: 4px;
	bottom: 3px;
	color: white;
	background: black;
	padding: 10px 20px;
	border-radius: 2px;
	font-family: 'Roboto Mono', monospace;
	cursor: pointer;
	transition: all .05s ease-out;
}
.button:active{
	position: relative;
	right: 2px;
	bottom: 1.5px;
	color: white;
	background: black;
	padding: 10px 20px;
	border-radius: 2px;
	font-family: 'Roboto Mono', monospace;
	cursor: pointer;
}
.button-border{
	border: 1px solid black;
	border-radius: 2px;
}
.font-icon{
	position: relative;
	left: 90%;
	top: 50px;
	font-size: 20px;
	margin-bottom: 10px;
	background: black;
	color: white;
	padding: 5px 5px;
	border-radius: 100%;
	opacity: 1;
}
.font-icon-none{
	position: relative;
	left: 90%;
	top: 50px;
	font-size: 20px;
	margin-bottom: 10px;
	background: black;
	color: white;
	padding: 5px 5px;
	border-radius: 100%;
	opacity: 0;
}
.view-none{
	display: none;
	opacity: 0;
}
</style>