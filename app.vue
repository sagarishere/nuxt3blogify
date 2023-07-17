<template>
  <div>
    <NuxtLayout>
      <NuxtPage />
    </NuxtLayout>
  </div>
</template>

<script setup>
// if dark theme then add dark class to body
if (localStorage.getItem("theme") === "dark") {
  document.body.classList.add("dark");
}
// if light theme then remove dark class from body
if (localStorage.getItem("theme") === "light") {
  document.body.classList.remove("dark");
}
</script>

<style lang="css">

body {
  background-color: #1f2937;
  transition: background-color 0.5s ease;
}

.page-enter-active {
  animation: bounce-in 1.8s;
}

.page-leave-active {
  animation: bounce-out 1.5s;
}

@keyframes bounce-in {
  0% {
    transform: scale(0);
  }
  80% {
    transform: scale(0.3);
  }
  100% {
    transform: scale(1);
  }
}

@keyframes bounce-out {
  0% {
    transform: scale(1);
  }
  60% {
    transform: scale(1.1);
  }
  100% {
    transform: scale(0);
  }
}

/* .page-enter-from {
  transform: translateX(-100%);
}
.page-leave-to {
  transform: translateX(100%);
} */
</style>