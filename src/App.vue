<template>
  
  <VueHeader
    v-if="showHeader"
  />

  <div v-show="showName">
    Nome: {{ name }}
  </div>

  <div v-if="accessLevel === 'admin'">Admin</div>
  <div v-else-if="accessLevel === 'tech'">Technician</div>
  <div v-else>User</div>
  
  <img alt="Vue logo" src="./assets/logo.png">
  
  <HelloWorld msg="Welcome to Your Vue.js App"/>
</template>

<script>
import HelloWorld from './components/HelloWorld.vue'
import VueHeader from './components/VueHeader.vue'

export default {
  name: 'App',
  components: {
    HelloWorld, VueHeader
  },

  data() {
    return {
      showHeader: true, 
      name: 'Ivan HS',
      showName: false,
      accessLevel: 'admin',
    }
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
