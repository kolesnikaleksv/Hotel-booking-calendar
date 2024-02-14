<script setup lang="ts">
// import {ref} from 'vue'

// const count = ref(0)

</script>

<template>
  <div class="header">
    <div class="header__container">
      <div class="header__logo">
        <img src="../assets/cerastes_cerastes.jpg">
        Amazing
      </div>
      <div class="header__nav">
        <ul>
          <li>Home</li>
          <li>Getting started</li>
          <li>Calendar</li>
          <li>About</li>
          <li>Contacts</li>
        </ul>
      </div>
      <div class="header__tools">Tools</div>
    </div>
  </div>
</template>

<style scoped lang="scss">
.header {
  @apply h-16 shadow-md;
  
  &__container {
    @apply flex flex-row justify-between items-center h-full;
  }

  &__logo {
    @apply flex flex-row h-3/5 text-green-400 items-center text-xl;

    img {
      @apply h-full mr-2;
    }
  }
  &__nav ul {
    @apply flex flex-row;

    li {
      @apply mx-4 my-2 text-lg cursor-pointer
      hover:shadow-lg;
    }
  }

  &__tools {
    @apply px-6 py-3 bg-green-500 rounded cursor-pointer text-white
    hover:shadow-xl;
  }
}
</style>