<script setup>
import { ref } from 'vue';

const awesome = ref(true)
const dynameId="appid"
const dynameClass="appclass"

function toggle() {
    awesome.value = !awesome.value
}

</script>
<template>
    <div class="hello">
        <p>&nbsp;</p>
        <div :id="dynameId" :class="dynameClass" v-if=awesome>test</div>
        <div :id="dynameId" :class="dynameClass" v-else>change</div>
        <button v-on:click="toggle">click change</button>
        <p>&nbsp;</p>
    </div>
</template>

<style>
.hello{
    background-color: #add8fb;
    border-radius: 25px;
    text-align: center;
}
.appclass{
    color: #ec261b;
    font-size: 30px;
}
</style>