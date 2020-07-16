<template>
   <quick :data="left" v-if="left.length"></quick>
   <li>{{flag}}</li>
   <quick :data="right" v-if="right.length"></quick>
   <!-- 有疑问、？？待研究！！！快排？？ -->
</template>
<script>
export default {
    name:'quick',
    props:['data'],
    setup(props){
        let flag = props.data[0]
        let left = []
        let right = []
        console.log(props.data)
        props.data.slice(1).forEach(v=>{
            v>flag? right.push(v): left.push(v)
        })
        return {left, right, flag}
    }
}
</script>