<script setup>
import { ref } from 'vue';
import HelloWorld from './components/HelloWorld.vue';
const message = ref('Hellow Vue!')

</script>

<template>
  <h1>{{ message }}</h1>
  <p>学习vue中……<br>此后作为一个web端的交互页面</p>
  <HelloWorld/>
</template>

