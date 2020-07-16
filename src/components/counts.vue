<template>
  <h1>{{state.count}} * 2={{double}}</h1>
  <h2>{{num}}</h2>
  <button @click="add">累加</button>
</template>
<script>
import { ref,reactive, computed,onMounted } from 'vue'


export default {
  // setup是新的选项，可以理解是comopsition的入口，函数内部在beforeCreate之前调用，函数返回的内容会作为模板渲染的上下文
  setup () {
    const state = reactive({
      count: 1
    })
    //reactive负责复杂数据结构，ref可以把基本的数据结构包装成响应式
    // ref包装的num，模板里可以直接写，js中修改的时候操作.value属性
    let num = ref(1)

    function add () {
      // console.log(state,num.value)
      state.count++;
      num.value+=5
    }
    const double = computed(() => state.count * 2)

    onMounted(()=>{
      console.log('mouted')
    })
    return { state, add, double ,num}
  }
}

// 拆分函数

</script>