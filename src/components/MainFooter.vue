<template>
  <div class="main-footer">
    <div class="main-footer__container">
      kolesnikaleksv@gmail.com
    </div>
  </div>
</template>

<script>
  export default {
    name: 'main-footer'
  }
</script>

<style lang="scss" scoped>
.main-footer {
  @apply flex justify-center items-center w-full h-16 bg-green-500 text-white;

  &__container {
    @apply flex h-3/5 w-full items-end justify-end;
  }
}
</style>