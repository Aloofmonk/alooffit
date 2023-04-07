<template>
  <div id="home" class="home">
    <MyNav/>
    <div class="big-text">
      <h1 v-motion :initial="{ opacity: 0, }" :enter="{ opacity: 1, }" :delay="100" >DISCOVER LIMITED SNEAKERS <span v-motion :initial="{ opacity: 0, }" :enter="{ opacity: 1, }" :delay="800">WITHOUT</span> <span v-motion :initial="{ opacity: 0, }" :enter="{ opacity: 1, }" :delay="900">LIMITATION</span>  </h1>
    </div>
    <div v-show="showDiv" class="station">
        <div v-motion :initial="{  y: -600 }" :enter="{ y: 0 }" :delay="300" class="home-link links"><a @click="activeLink = 'home'" :class="[activeLink === 'home' ? 'active' : '']" class='links' href="#home"><font-awesome-icon icon="house" /></a></div>
        <div v-motion :initial="{ y: -600 }" :enter="{ y: 0 }" :delay="500" class="dots links"><a @click="activeLink = 'about'" :class="[activeLink === 'about' ? 'active' : '']" class='links' href="#about"><font-awesome-icon icon="circle" /></a></div>
        <div v-motion :initial="{ y: -600 }" :enter="{ y: 0 }" :delay="700" class="dots links"><a @click="activeLink = 'article'" :class="[activeLink === 'article' ? 'active' : '']" class='links' href="#article"><font-awesome-icon icon="circle" /></a></div>
        <div v-motion :initial="{ y: -600 }" :enter="{ y: 0 }" :delay="900" class="dots links"><a @click="activeLink = 'product'" :class="[activeLink === 'product' ? 'active' : '']" class='links' href="#product"><font-awesome-icon icon="circle" /></a></div>
        <div v-motion :initial="{ y: -600 }" :enter="{ y: 0 }" :delay="1100" class="dots links"><a @click="activeLink = 'blog'" :class="[activeLink === 'blog' ? 'active' : '']" class='links' href="#blog"><font-awesome-icon icon="circle" /></a></div>
        <div v-motion :initial="{ y: -600 }" :enter="{ y: 0 }" :delay="1300" class="links phone"><a @click="activeLink = 'contact'" :class="[activeLink === 'contact' ? 'active' : '']" class='links' href="#contact"><font-awesome-icon icon="phone" /></a></div>
    </div>
    <div class="home-card">
        <div v-motion :initial="{ y: 300 }" :enter="{ y: 0 }" :delay="700" class="card1 card">
          <img src="../images/vans.png" alt="">
        </div>
      <div v-motion :initial="{ y: 300 }" :enter="{ y: 0 }" :delay="800" class="card2 card"><img src="../images/puma.png" alt=""></div>
      <div v-motion :initial="{ y: 300 }" :enter="{ y: 0 }" :delay="900" class="card3 card"><img src="../images/nike_318-565950.webp" alt=""></div>
      <div v-motion :initial="{ y: 300 }" :enter="{ y: 0 }" :delay="1000" class="card4 card"><img src="../images/adidas_318-565831.avif" alt=""></div>
    </div>
  </div>
</template>

<script scoped>
import MyNav from './MyNav.vue';
import { ref, onMounted } from 'vue';


export default {
  name: 'MyHome',
  components: {
    MyNav,
  },
  props: {
    
  },
  data(){
    return{
      activeLink: '',
    }
  },
   setup() {
    const showDiv = ref(false);

    onMounted(() => {
      window.addEventListener('scroll', function () {
        if (window.scrollY > 200) {
          showDiv.value = true;
        }else{
          showDiv.value = false
        }
      });
    });

    // Code for the component goes here
    return {
      showDiv,
    };
  },
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
 @import url('https://fonts.googleapis.com/css2?family=Oswald:wght@600&family=Roboto+Mono&family=Teko&display=swap');

 /* #home{
  
 } */
.big-text{
  height: 45.5%;
  font-size: 55px;
  box-sizing: border-box;
  padding: 20px 68px;
  text-align: left;
  font-family: 'Teko', sans-serif;
  margin-bottom: 10px;
}

h1{
  line-height: 0.92;
  display: inline-block;
  line-break:loose;
  word-spacing: 8px;
  letter-spacing: 3px;
}
.home-card{
  display: grid;
  grid-template-columns: repeat(4, 1fr);
  border: 2px solid #bbbaba;
}

.card1{
  border: 2px solid #bbbaba;
  height: 288px;
  padding-left: 65px;
  background: rgb(244,242,242);
	transition: all .5s ease-out;
}
.card2{
  border: 2px solid #bbbaba;
  height: 288px;
  padding-left: 65px;
  background: rgb(244,242,242);
	transition: all .5s ease-out;
}
.card3{
  border: 2px solid #bbbaba;
  height: 288px;
  padding-top: 80px;
  background: rgb(244,242,242);
	transition: all .5s ease-out;
}
.card4{
  border: 2px solid #bbbaba;
  height: 288px;
  padding-left: 65px;
  padding-top: 65px;
  background: rgb(244,242,242);
	transition: all .5s ease-out;
}
.card{
  border: 2px solid #bbbaba;
  height: 288px;
  padding-left: 65px;
  padding-top: 40px;
  background-position: right bottom;
	transition: all .5s ease-in-out;
}
.card:hover{
  background: black;
  background: linear-gradient(to right, black 50%,  rgb(244,242,242)50%);
	background-size: 200% 100%;
	background-position: left bottom;
	cursor: pointer;
	border-radius: 2px;
}
.card:hover img{
  filter: invert(90%);
}

img{
  width: 200px;
}
.station{
  position: fixed;
  right: 30px;
  bottom: 60px;
  backdrop-filter: blur(5px);
  background: rgba(0,0,0,0.4);
  border-radius: 10px;
  padding: 30px 10px;
  z-index: 1000;
}
.links{
  color: rgb(255, 253, 253);
  transition: all .3s ease-in-out;
}
.home-links{
  padding-bottom: 30px;
}
.dots{
  font-size: 8px;
  padding: 7px 4px;
}
.phone{
  padding: 5px 0;
}
.active{
  color: red;
}
</style>
