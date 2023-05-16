<template>
  <div class="all">
    <MyLoading v-if="isLoading"></MyLoading>
    <div v-else>
  
      <MyHome/>
      <MyAbout/>
      <!-- <MyRelease/> -->
      <MyNewArticle/>
      <MyProduct/>
      <MyBlog/>
      <MyContact/>
    </div>
  </div>
  <p class="mobile">Mobile view not available yet. Please use a PC for optimal experience!</p>
</template>

<script>
import MyHome from './components/MyHome.vue'
import MyAbout from './components/MyAbout.vue'
import MyProduct from './components/MyProduct.vue'
import MyNewArticle from './components/MyNewArticle.vue';
import MyLoading from './components/MyLoading.vue';
import MyBlog from './components/MyBlog.vue';
import MyContact from './components/MyContact.vue';
// import MyRelease from './components/MyRelease.vue';

export default {
  name: 'App',
  components: {
    MyHome,
    MyAbout,
    MyProduct,
    MyNewArticle,
    MyBlog,
    MyLoading,
    MyContact
    // MyRelease
},
  data() {
    return {
      isLoading: true,
    }
  },
  mounted() {
    // Simulate a loading delay
    setTimeout(() => {
      this.isLoading = false
    }, 3000)
  }
}
</script>

<style>
@import url('https://fonts.googleapis.com/css2?family=Delicious+Handrawn&family=Oswald:wght@600&family=Roboto+Mono&family=Teko&display=swap');

* {
  /* overflow: hidden; */
  padding: 0;
  margin: 0;
  box-sizing: border-box;
  scroll-behavior: smooth;
}
#app{
  overflow: hidden;

}
body {
  scroll-snap-type: y mandatory;
}

section {
  height: 100vh;
  scroll-snap-align: start;
}

.mobile{
    visibility: hidden;
  }

::-webkit-scrollbar {
	width: 6px;
}

/* Change the background color of the scrollbar track */
::-webkit-scrollbar-track {
	background-color: transparent;
}

/* Change the color and style of the scrollbar thumb */
::-webkit-scrollbar-thumb {
	background-color: #888;
	border-radius: 5px;
}

/* Change the color and style of the scrollbar thumb when hovered */
::-webkit-scrollbar-thumb:hover {
	background-color: #555;
}
@media screen and (max-width: 1187px){
  .all{
    display: none;
  }

  #app{
    height: 100vh;
    display: flex;
    justify-content: center;
    align-items: center;
    font-family: 'Roboto Mono', monospace;
  }

  .mobile{
    visibility: visible;

  }
}
</style>
