<script setup>
defineProps(["id", "title", "body"]);
const truncateDescription = (desc, wc) => desc ? desc.split(" ").slice(0, wc).join(" ") + (desc.split(" ").length > wc ? '...' : '') : "";
</script>

<template>
    <div
      class="bg-gray-600 rounded-lg shadow-lg overflow-hidden flex flex-col md:flex-row mx-auto py-4 max-w-5xl mt-3 hover:shadow-indigo-500/40"
    >
      <div class="w-full md:w-1/3 p-4">
        <img
          src="/images/banner.jpg"
          alt="Post Image"
          class="w-full h-auto object-cover hover:hue-rotate-180"
        />
      </div>
      <div class="w-full md:w-2/3 px-6 py-4 ease-in-out duration-300 text-stone-300">
        <h2 class="text-2xl font-bold mb-2">{{ title }}</h2>
        <p class="text-base mb-4 text-stone-300">
          {{ truncateDescription(body, 40) }}
        </p>
        <NuxtLink
          :to="'/posts/' + id"
          class="bg-slate-500 hover:bg-slate-700 font-bold py-2 px-4 rounded"
        >
          Read More
        </NuxtLink>
      </div>
    </div>
  </template>
  
  <style lang="css" scoped></style>