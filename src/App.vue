<template>
  <div id="app">
    <headerTop></headerTop>
    <addtask></addtask>
  </div>
</template>

<script>
import HeaderTop from './components/HeaderTop.vue'
import AddTask from './components/AddTask.vue'

export default {
  name: 'App',
  components: {
    'headerTop': HeaderTop,
    'addtask' : AddTask
  }
}
</script>

<style>
  *,::before, ::after{
  margin: 0;
  padding: 0;
  }
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: #2c3e50;
}
</style>
