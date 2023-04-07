<template>
	<div class="blog" id="blog">
		<div class="top-div">
			<div class="text">BLOGS</div>
			<div class="button-border">
				<div @click="more = !more, horizontalScrollUsed = !horizontalScrollUsed" class="button">
					{{ more === true ? 'RESTORE' : 'VIEW MORE' }}
				</div>
			</div>
		</div>
		<font-awesome-icon :class="[horizontalScrollUsed === true ? 'font-icon-none' : 'font-icon']" icon="arrow-right"
			shake />
		<div @scroll="onScroll" class="bottom-div">
			<div :class="[more === true ? 'view-none' : 'card']">
				<div class="top-text">SPORT</div>
				<img src="../images/gianis.webp" alt="">
				<div class="bottom-text">PROPEL YOUR GAME FORWARD</div>
			</div>
			<div :class="[more === true ? 'view-none' : 'card']">
				<div class="top-text">LADIES</div>
				<img src="../images/pswalk.jpg" alt="">
				<div class="bottom-text">MOVE TOWARDS YOUR GOAL</div>
			</div>
			<div :class="[more === true ? 'view-none' : 'card']">
				<div class="top-text">LIFESTYLE</div>
				<img src="../images/psdress.jpg" alt="">
				<div class="bottom-text">WE WEAR DRESSES TO</div>
			</div>
			<div :class="[more === true ? 'view-none' : 'card']">
				<div class="top-text">KIDS</div>
				<img src="../images/pskids.jpg" alt="">
				<div class="bottom-text">THE LITTLE ONES</div>
			</div>
			<div :class="[more === true ? 'view-none' : 'card']">
				<div class="top-text">FRIENDS</div>
				<img src="../images/psfriends.jpg" alt="">
				<div class="bottom-text">MAKE MEMORIES</div>
			</div>
			<div :class="[more === true ? 'view-none' : 'card']">
				<div class="top-text">LEISURE</div>
				<img src="../images/pswalk.jpg" alt="">
				<div class="bottom-text">PEACE AND QUIET TIME</div>
			</div>
			<div class="card">
				<div class="top-text">SPORT</div>
				<img src="../images/gianis.webp" alt="">
				<div class="bottom-text">PROPEL YOUR GAME FORWARD</div>
			</div>
			<div class="card">
				<div class="top-text">SPORT</div>
				<img src="../images/gianis.webp" alt="">
				<div class="bottom-text">PROPEL YOUR GAME FORWARD</div>
			</div>
			<div class="card">
				<div class="top-text">SPORT</div>
				<img src="../images/gianis.webp" alt="">
				<div class="bottom-text">PROPEL YOUR GAME FORWARD</div>
			</div>
			<div class="card">
				<div class="top-text">SPORT</div>
				<img src="../images/gianis.webp" alt="">
				<div class="bottom-text">PROPEL YOUR GAME FORWARD</div>
			</div>
		</div>
	</div>
</template>

<script>
export default {
	name: 'MyNewArticle',
	data() {
		return {
			horizontalScrollUsed: false,
			more: false
		}
	},
	methods: {
		onScroll(event) {
			if (event.target.scrollLeft > 0) {
				this.horizontalScrollUsed = true;
			} else {
				this.horizontalScrollUsed = false
			}
		}
	}


}

</script>


<style scoped>
@import url('https://fonts.googleapis.com/css2?family=Delicious+Handrawn&family=Oswald:wght@200;600&family=Roboto+Mono&family=Teko&display=swap');

.blog {
	padding: 65px 0;
}

.top-div {
	display: flex;
	justify-content: space-between;
	height: 30%;
	border-bottom: 1px solid black;
	align-items: center;
	padding: 0 55px;
}

.bottom-div {
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

.text {
	font-family: 'Teko', sans-serif;
	font-size: 80px;
}

img {
	width: 200px;
	height: 300px;
	object-fit: fill;
	border-radius: 5px;
}


.card {
	display: inline-block;
	/* border: 1px solid black; */
	margin-right: 20px;
}

.button {
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

.button:active {
	position: relative;
	right: 0px;
	bottom: 0px;
	color: white;
	background: black;
	padding: 10px 20px;
	border-radius: 2px;
	font-family: 'Roboto Mono', monospace;
	cursor: pointer;
}

.button-border {
	border: 1px solid black;
	border-radius: 2px;
}

.top-text {
	font-family: 'Teko', sans-serif;
	/* background: white; */
	position: relative;
	top: 40px;
	left: 10px;
	color: white;
	width: 40px;
	font-size: 20px;
	padding: 2px 2px;
	border-radius: 10px;
}

.bottom-text {
	font-family: 'Oswald', sans-serif;
	width: 180px;
	word-break: break-all;
	bottom: 50px;
	left: 10px;
	position: relative;
	color: white;
	background: rgba(100, 100, 100, 0.3);
}
.font-icon {
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

.font-icon-none {
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

.view-none {
	display: none;
	opacity: 0;
}
</style>