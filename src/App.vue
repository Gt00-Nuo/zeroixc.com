<script setup>
import { ref } from 'vue';
import HelloWorld from './components/HelloWorld.vue';
import ListDemo from './components/ListDemo.vue';
const audio = ref()
const plays = () => {
  if (audio.value) {
    audio.value.play();
  }
}
const startAudio = () => {
  plays();
}
const pauses = () => {
  if (audio.value) {
    audio.value.pause();
  }
}
const pauseAudio = () => {
  pauses();
}
const appMain = ref('appmain')
const message = "Yezi"
const tags = "top_tags"
</script>

<template>
  <div :class="tags">
    <ul>
      <a href="">
        <ol :class="tags">首页</ol>
      </a>
      <a href="">
        <ol :class="tags">首页</ol>
      </a>
      <a href="">
        <ol :class="tags">首页</ol>
      </a>
      <a href="">
        <ol :class="tags">首页</ol>
      </a>
      <a href="">
        <ol :class="tags">首页</ol>
      </a>
      <a href="">
        <ol :class="tags">首页</ol>
      </a>
    </ul>
  </div>
  <br>
  <div :class="appMain">
    <h1>{{ message }}</h1>
    <button @click="startAudio">播放</button>
    <button @click="pauseAudio">暂停</button>
    <audio ref="audio" currentTime>
      <source src="../music/揉碎夜的光--代诗琪.mp3" type="audio/ogg" />
    </audio>
    <p>学习vue中……<br>此后作为一个web端的交互页面</p>
  </div>
  <HelloWorld  class="HelloWrold"/>
  <ListDemo/>
</template>

<style>
.appmain{
  background-color: #2f90ba;
  width: 100%;
  border-radius: 25px;
  text-align: center;
}
.appmain>button{
  background-color: #bbd6e1;
  color: #000000;
  width: 40px;
  height: 40px;
  border-radius: 5px;
}
.top_tags{
  float: inline-start;
  display: block;
}
.top_tags>ul>a{
  color: #000;
}
</style>