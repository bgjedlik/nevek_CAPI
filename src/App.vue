<script setup>
import NameList from './components/NameList.vue'
import InputForm from './components/InputForm.vue'

import { ref } from "@vue/reactivity";

let names = ref(["józsi", "Béla"]);
//console.log(names.value[0]);

const addToList = (data)=>{
  names.value.push(data)
 }

</script>

<template>
  <input-form @addToList="addToList"/>

  <name-list :names="names"/>
  <!-- {{ names }} -->

  
</template>

<style scoped>
</style>
