<script setup>
import { ref } from 'vue';

let qty =ref(2) 
function addValue(){
  qty.value++
  console.log(qty)
}
function minValue(){
  if(qty.value >0){
    qty.value--
  }
 
  console.log(qty)
}
</script>

<template>
  <div class="wrapper">
    <div class="profile">
      <div class="ballon" v-if="qty>0">{{ qty }}</div>
    </div>

    <div class="button-wrapper">
      <div class="button" @click="minValue">-</div>
      <div class="button" @click="addValue">+</div>
    </div>
    <div v-if="qty>0">me escribieron 😊😊😊😊😊😊😊😊😊😊</div>
    <div v-if="qty==0">nadie me escribe 😢😢😢😢😢😢😢😢😢😢😢😢😢😢😢</div>
  </div>
</template>

<style scoped>
.button:hover {
  cursor: pointer;
  background-color: #dbf227;
}
.button {
  background-color: #9fc131;
  display: inline-block;
  padding: 4px 0;
  border-radius: 4px;
  width: 32px;
  margin: 0 8px;
}
.button-wrapper {
  text-align: center;
  margin-top: 16px;
  margin-bottom: 16px;
}
.ballon {
  position: absolute;
  top: 0;
  right: 0;
  width: 32px;
  height: 32px;
  background-color: #9fc131;
  border-radius: 100%;
  display: flex;
  justify-content: center;
  align-items: center;
  color: white;
}
.wrapper {
  overflow: hidden;
  padding-top: 18px;
  background-color: #042940;
  width: 60%;
  border-radius: 12px;
  margin: 0 auto;
}
.profile {
  background-image: url(https://elpilon.com.co/wp-content/uploads/2022/06/MARATON-1-CORTESIA-1.jpg);
  background-size: cover;
  position: relative;
  background-color: #005c53;
  width: 160px;
  height: 160px;
  margin: 0 auto;
  border-radius: 100%;
}
</style>
