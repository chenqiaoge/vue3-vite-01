<template>
  <img alt="Vue logo" src="./assets/logo.png" />
  <HelloWorld msg="Hello Vue 3.0 + Vite" />
  <Counts />
  <ul>
    <FragmentDemo :data="[5,3,1,6,9,4,2,8,0,5]" />
    <!-- vue3 新增的组件Fragment（根元素不限制一个）, Teleport（适合弹窗）, Suspense（异步组件） -->
  </ul>
  <ul>
    <QuickDemo :data="[5,3,1,6,9,4,2,8,0]" />
  </ul>
</template>

<script>
import HelloWorld from './components/HelloWorld.vue'
import Counts from './components/counts.vue'
import FragmentDemo from './components/fragmentDemo.vue'
import QuickDemo from './components/testQuick.vue'

export default {
  name: 'App',
  components: {
    HelloWorld,Counts,FragmentDemo,QuickDemo
  }
}
</script>
