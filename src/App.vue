<script setup>
import { ref } from 'vue';
import HelloWorld from './components/HelloWorld.vue';
const message = ref('Hellow Vue!')

</script>

<template>
  <h1>{{ message }}</h1>
  <HelloWorld/>
</template>

