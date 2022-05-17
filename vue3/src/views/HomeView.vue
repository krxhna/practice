<script setup>
import { ref } from "vue";
import { useRouter } from 'vue-router';

const router = useRouter();



let name = ref(1);

function alert() {
  name.value = name.value * 2;
}

function gotonmeow() {
   router.push("/meow");
}
</script>

<template>
  <div class="text-5xl h-screen flex-col items-center flex justify-center">
    <div class="d">{{ name }}</div>
    <button class="p-2 bg-green-400" @click="gotonmeow">click</button>
  </div>
</template>
