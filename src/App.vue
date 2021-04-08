<template>
  <div id="app">
    <!-- <img alt="Vue logo" src="./assets/logo.png"> -->
    <Header />
    <TodoList/>
    <Footer  title="TodoList"/>
    <HelloWorld msg=""/>
  </div>
</template>

<script>
import HelloWorld from './components/HelloWorld.vue'
import Header from './components/Header.vue'
import TodoList from  './components/TodoList.vue'
import Footer from  './components/Footer.vue'

export default {
  name: 'App',
  components: {
    HelloWorld,
    Header,
    TodoList,
    Footer,
  },

}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 0px;
  font-size: 24px;
  
}
</style>
