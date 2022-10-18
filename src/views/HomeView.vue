<template>
  
  <div class="home">
    
    <img alt="Vue logo" src="../assets/logo.png">
    <HelloWorld msg="Welcome to Your Vue.js App"/>
  </div>
  <div class="comp">
    <FirstComponent></FirstComponent>
  </div>
</template>

<script>
// @ is an alias to /src
import HelloWorld from '@/components/HelloWorld.vue'
import FirstComponent from '@/components/FirstComponent.vue';

export default {
  name: 'HomeView',
  components: {
    HelloWorld,
    FirstComponent
}
}
</script>

<style>

</style>