<template>
    <input type="checkbox">全选/全不选
    <ul>
        <li v-for="item in list">
            <input type="checkbox">
        </li>
    </ul>
</template>

<script lang='ts' setup>
import {reactive, toRefs } from 'vue'
// let {list, num ,a} = toRefs(reactive({
//     list:[10,20,30,40],
//     num:20,
//     a:{

//     }
// }))

let data = reactive({
    list:[10,20,30,40]
})
let {list} = toRefs(data)
</script>

<style lang = "less" scoped>
    
</style>