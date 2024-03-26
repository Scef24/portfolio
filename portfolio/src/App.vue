<script>
import HelloWorld from './components/HelloWorld.vue';
import About from './components/about.vue'

export default{ 
  name:'App',
  components:{
    HelloWorld,
    About
  }
}
</script>

<template>


<div id = 'app'>
<nav>
  <router-link to="/">Home</router-link>
  <router-link to="/about">About</router-link>
</nav>
<RouterView></RouterView>
</div>
</template>

<style>
</style>