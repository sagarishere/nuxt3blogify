<template>
    <div class="bg-slate-900 min-h-screen">
        <Navbar />
        <Hero />
        <slot />
    </div>
</template>

<script setup>
useHead({
    title: 'Blogify',
    meta: [
        {
            name: 'description',
            content: 'Blogify is a blog application built with Nuxt.js'
        }
    ]
});

</script>

<style lang="scss" scoped>

</style>