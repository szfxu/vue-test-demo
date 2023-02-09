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
    checkList:[false, false, false, false]
})
let {list,checkList} = toRefs(data)
let checkAll = computed({
    get(){
        // checkAll 是受这个checkList 这个数组的影响
        // checkList 只要包含一个false，那应该返回就是false
        // 得到的是一个真的，true
       return !data.checkList.includes(false)
    },
    set() {

    }
})
</script>

<style lang = "less" scoped>
    
</style>