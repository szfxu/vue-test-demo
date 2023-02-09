<template>
    <input type="checkbox">全选/全不选
    <ul>
        <li></li>
    </ul>
</template>

<script lang='ts' setup>
import {reactive  } from 'vue'

let {list, num ,a} = toRefs( reactive({
    list:[10,20,30,40],
    num:20,
    a:{

    }
}))
</script>

<style lang = "less" scoped>
    
</style>