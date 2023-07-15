<template>
  <div>
    <NuxtLayout>
      <NuxtPage />
    </NuxtLayout>
  </div>
</template>

<script setup>

</script>

<style lang="css" scoped>
.page-enter-active, .page-leave-active {
  transition: all 0.2s;
}
.page-enter-from, .page-leave-to {
  filter: grayscale(1);
}
</style>