<template>
  <div id="home" class="home">
    <MyNav/>
    <div class="big-text">
      <h1>UNCOVER LIMITED SNEAKERS WITHOUT LIMITATION</h1>
    </div>
    <div v-show="showDiv" class="station">
        <div class="links"><a class='links' href="#home"><font-awesome-icon icon="house" /></a></div>
        <div class="dots links"><a class='links' href="#about"><font-awesome-icon icon="circle" /></a></div>
        <div class="dots links"><a class='links' href="#article"><font-awesome-icon icon="circle" /></a></div>
        <div class="dots links"><a class='links' href="#product"><font-awesome-icon icon="circle" /></a></div>
        <div class="dots links"><a class='links' href="#blog"><font-awesome-icon icon="circle" /></a></div>
        <div class="links phone"><a class='links' href="#contact"><font-awesome-icon icon="phone" /></a></div>
    </div>
    <div class="home-card">
        <div class="card1 card">
          <img src="../images/vans.png" alt="">
        </div>
      <div class="card2 card"><img src="../images/puma.png" alt=""></div>
      <div class="card3 card"><img src="../images/swoosh.png" alt=""></div>
      <div class="card4 card"><img src="../images/addidas.png" alt=""></div>
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
  /* padding-top: 65px; */
  background: rgb(244,242,242);
	transition: all .5s ease-out;
}
.card2{
  border: 2px solid #bbbaba;
  height: 288px;
  padding-left: 65px;
  /* padding-top: 65px; */
  background: rgb(244,242,242);
	transition: all .5s ease-out;
}
.card3{
  border: 2px solid #bbbaba;
  height: 288px;
  /* padding-left: 65px; */
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
	transition: all .3s ease-in-out;
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
  right: 50px;
  bottom: 60px;
  backdrop-filter: blur(5px);
  background: rgba(0,0,0,0.4);
  border-radius: 10px;
  padding: 20px 10px;
  z-index: 1000;
}
.links{
  color: rgb(255, 253, 253);
}
.dots{
  font-size: 8px;
  padding: 5px 4px;
}
.phone{
  padding: 5px 0;
}
</style>
