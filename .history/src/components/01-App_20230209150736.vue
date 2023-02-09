<template>
    <input type="checkbox" v-model="checkAll">全选/全不选
    <ul>
        <li v-for="item,index in list" :key="index">
            <input type="checkbox" v-model="checkList[index]">{{item}}
        </li>
    </ul>
</template>

<script lang='ts' setup>
import {reactive, toRefs, ref, computed } from 'vue'
// let {list, num ,a} = toRefs(reactive({
//     list:[10,20,30,40],
//     num:20,
//     a:{

//     }
// }))

let data = reactive({
    list:[10,20,30,40],
    checkList:[false, false, true, false]
})
let {list,checkList} = toRefs(data)
let checkAll = computed({

})
</script>

<style lang = "less" scoped>
    
</style>