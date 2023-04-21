<template>
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
@import url('https://fonts.googleapis.com/css2?family=Oswald:wght@600&family=Roboto+Mono&family=Teko&display=swap');

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
</style>
