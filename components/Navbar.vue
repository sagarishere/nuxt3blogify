<template>
    <div>
        <nav class="bg-gray-800">
        <div class="max-w-7xl mx-auto px-2 sm:px-6 lg:px-8">
            <div class="relative flex items-center justify-between h-16">
                <div class="hidden sm:block sm:ml-6">
                    <div class="flex space-x-4">
                        <!-- Hoem Tab -->
                        <NuxtLink to="/" class="text-white px-3 py-2 rounded-md text-sm font-medium" active-class="bg-gray-900"> Home </NuxtLink>
                        <NuxtLink to="/about" class="text-white px-3 py-2 rounded-md text-sm font-medium" active-class="bg-gray-900"> About </NuxtLink>
                        <NuxtLink to="/contact" class="text-white px-3 py-2 rounded-md text-sm font-medium" active-class="bg-gray-900"> Contact </NuxtLink>
                    </div>
                </div>
            </div>
        </div>
    </nav>
    </div>
</template>

<script setup>

</script>

<style lang="scss" scoped>

</style>