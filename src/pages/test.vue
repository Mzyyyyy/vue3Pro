<template>
    <JsxCmpt></JsxCmpt>
</template>

<script setup>
import {ref, reactive,computed,watchEffect } from 'vue';
import JsxCmpt from './jsx.jsx'
let small = ref(0)
let obj = reactive({
    count:111
})
let newVal = computed(()=>{
    return obj.count*2
})
// obj.count = 444
watchEffect(()=>{
    console.log(small.value,898989)
    console.log(newVal.value,898989)
    console.log(obj.count,898989)
})
obj.count = 444
</script>