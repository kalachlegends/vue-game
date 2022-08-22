<template lang="">
    <div v-if="posts.length > 0">
        <h3> список Пользователей</h3>
       <post-item 
       :key="post.id" 
       v-for="post in posts" 
       :post="post" 
       @remove="$emit('remove',post)" />
    </div>
    <h2 v-else="">

    Список Пользователей пуст
    </h2>
</template>
<script>
import PostItem from '@/components/postItem'
export default {
    components: { PostItem },
    props: {
        posts: {
            type: Array,
            required: true

        }
    }
}
</script>
<style scoped>
.post {
    padding: 10px;
    border: 1px solid teal;
    margin-top: 15px;
}
</style>