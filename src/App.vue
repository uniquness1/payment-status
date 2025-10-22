<template>
  <main class="max-w-md w-full mx-auto bg-[#fbfbfb] rounded p-6 my-5">
    <mainHeading />
    <people />
    <div class="h-[680px]"></div>
    <mainFooter />
  </main>
</template>
<script setup>
import mainHeading from './components/mainHeading.vue';
import people from './components/tripPeople.vue';
import mainFooter from './components/mainFooter.vue';
</script>