<template lang="">
  <div class="post">
            <div><strong>Название:</strong> {{ post.title }}</div>
            <div><strong>Описание:</strong> {{ post.body }}</div>
            <my-button @click="$emit('remove', post)">Удалить</my-button>
        </div>
</template>
<script>


export default {
    props: {
        post: {
            type: Object,
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