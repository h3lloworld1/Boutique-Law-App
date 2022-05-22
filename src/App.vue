<template>
  <div id="app">
    <NavBar/>
    <router-view :key="$route.name"/>
    <FooterMain/>
  </div>
</template>


<script>
import NavBar from "./components/NavBar.vue"
import FooterMain from "./components/FooterMain.vue"




export default {
  name: 'App',
   data () {
    return {
      greeting: 'Hello'
    }
  },
  components: {
    NavBar,
    FooterMain,

  }
}
</script>

<style>
@import url('https://fonts.googleapis.com/css2?family=Raleway:wght@300;400;500;600;700&display=swap');
#app {
  
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  
  
  
}


</style>
