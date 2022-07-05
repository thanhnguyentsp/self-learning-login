<script setup lang="ts">
import { ref } from 'vue';
import LoginForm, { FormSubmit } from './components/LoginForm.vue';

const onSumit = ref((e: FormSubmit) => {
  console.log(e);
  
  window.alert(`Logged in with user ${e.name}`)
})
</script>

<template>
  <div class="app w-full flex justify-center items-center">
    <LoginForm @submit="onSumit"></LoginForm>
  </div>
</template>

<style >
.app {
  height: 100vh;
  background-image: url('https://img.freepik.com/free-vector/japanese-wave-line-art-landscape-background-abstract-mountain-banner-design-pattern-vector-illustration-geometric-poster_90220-714.jpg?w=1480&t=st=1657012673~exp=1657013273~hmac=b6533ef118b70bde3538dd160d0bcaa0210099047a483aeadea45fa919584d2c');
  background-repeat: no-repeat;
  background-size:cover;
}
</style>