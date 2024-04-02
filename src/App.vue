<template>
<div id="app">
    <router-link to="/">Home</router-link>
    
    <router-link to="/about">About</router-link>
    <router-view></router-view>
  </div>
  <img alt="Vue logo" src="./assets/logo.png">
  <HelloWorld msg="Welcome to Your Vue.js App"/>
  <DemoComp/>
  <ConditionalTest/>
  <ListRenderingComponent/>
  <TestEvents/>
  <ParentComp/>
</template>

<script>
import HelloWorld from './components/HelloWorld.vue'
import DemoComp from './components/DemoComp.vue'
import ConditionalTest from './components/ConditionalTest.vue'
import ListRenderingComponent from './components/ListRenderingComponent.vue'
import TestEvents from './components/TestEvents.vue'
import ParentComp from './components/ParentComp.vue'


export default {
  name: 'App',
  components: {
    HelloWorld,
    DemoComp,
    ConditionalTest,
    ListRenderingComponent,
    TestEvents,
    ParentComp
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
