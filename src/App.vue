<template>
  <Sidebar></Sidebar>
  <PlayerContent></PlayerContent>
</template>

<script>
import HelloWorld from './components/HelloWorld.vue'
import Sidebar from './components/Sidebar.vue'
import PlayerContent from './components/PlayerContent.vue'
import Modal from './components/Modal.vue'

export default {
  name: 'App',
  components: {
    HelloWorld,
    Sidebar,
    PlayerContent,
    Modal
  }
}
</script>

<style>
*{
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-aldign: center;
  color: #2c3e50;
}
</style>

