<script setup>
import { ref } from 'vue';

// export default{
//     data(){
//         return{
//             dynameClass:"appclass",
//             dynameId:"appid",
//             isButtonDisabled:false,
//             objectOfAttres:{
//                 class:"appclass",
//                 id:"appid"
//             }
//         }
//     }
// }
const awesome = ref(false)
const dynameId="appid"
const dynameClass="appclass"

function toggle() {
    awesome.value = !awesome.value
}

</script>
<template>
    <div :id="dynameId" :class="dynameClass" v-if=awesome>objectOfAttres</div>
    <div :id="dynameId" :class="dynameClass" v-else>test</div>
    <button v-on:click="toggle">click</button>
</template>

<style>

.appclass{
    color: #ec261b;
    font-size: 30px;
}
</style>