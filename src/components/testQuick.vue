<template>
  <!-- <ul> -->
    <quick :data="left" v-if="left.length"></quick>
    <li>{{flag}}</li>
    <quick :data="right" v-if="right.length"></quick>
    <!-- 有疑问、？？待研究！！！ -->
  <!-- </ul> -->
  <!-- <div @click="quickSort">quick sort</div> -->
</template>
<script>
import { ref,reactive,onMounted } from 'vue'
export default {
    name:'quick', // 这个name必须是quick？？
    props:['data'],
    setup(props){
      let left = ref([])
      let right = ref([])
      let flag = ref(props.data[0])
        function quickSort(){
          // flag = props.data[0]
          console.log('11',flag,left,right)
          props.data.slice(1).forEach(v=>{
            v>flag.value? right.value.push(v): left.value.push(v)
          })
        }
        onMounted(()=>{
          console.log('---')
          setTimeout(()=>{
            quickSort()
          },3000)
        })
        return {left, right, flag,quickSort}
    }
}
</script>