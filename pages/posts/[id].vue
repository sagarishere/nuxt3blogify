<script setup>
definePageMeta({
    layout: 'custom',
});

const route = useRoute();
const { data: post, error, pending } = useLazyFetch(`https://dummyjson.com/posts/${route.params.id}`)
useHead({
    title: `Post ID ${route.params.id}`,
});

const setHead = (title) => {
    console.log(title);
    useHead({
        title,
    });
}

</script>
<template>
     <div class="flex flex-col items-center h-screen bg-gray-900">
        <div v-if="error" class="text-2xl text-white">
            An error occured... {{ error }}
        </div>
        <div v-else-if="pending" class="text-2xl text-white">
            <LoadingBlock />
        </div>
        <div v-else :on-load="setHead(post.title)">
            <PostDetail :id="post.id" :title="post.title" :body="post.body" />
        </div>
    </div>
</template>


<style lang="css" scoped>

</style>