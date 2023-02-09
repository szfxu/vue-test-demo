<template>
    <input type="checkbox" v-model="checkAll">全选/全不选
    <ul>
        <li v-for="item in list">
            <input type="checkbox" v-model="checkList[index]">{{item}}
        </li>
    </ul>
</template>

<script lang='ts' setup>
import {reactive, toRefs, ref } from 'vue'
// let {list, num ,a} = toRefs(reactive({
//     list:[10,20,30,40],
//     num:20,
//     a:{

//     }
// }))
let checkAll = ref(false)
let data = reactive({
    list:[10,20,30,40],
    checkList:[false, false, false, false]
})
let {list,checkList} = toRefs(data)
</script>

<style lang = "less" scoped>
    
</style>