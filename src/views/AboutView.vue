<script setup>
const title = "This is about page"
const isButtonDisabled = false;
</script>
<template>
  <div class="about">
    <h1 >{{title}}</h1>
    <button :disabled="isButtonDisabled">Button</button>
  </div>
</template>

<style>
@media (min-width: 1024px) {
  .about {
    min-height: 100vh;
    display: flex;
    align-items: center;
  }
}
</style>
