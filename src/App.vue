<template>
  <img alt="Vue logo" src="./assets/logo.png" />
  <HelloWorld msg="Hello Vue 3.0 + Vite" />
  <Counts />
</template>

<script>
import HelloWorld from './components/HelloWorld.vue'
import Counts from './components/counts.vue'

export default {
  name: 'App',
  components: {
    HelloWorld,Counts
  }
}
</script>
