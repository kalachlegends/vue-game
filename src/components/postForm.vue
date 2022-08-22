<template lang="">
        <div>
            <h4>Создание поста</h4>
            <form @submit.prevent>
                <my-input  v-model="post.title" class="input" type="text" placeholder="Название"/>
                <my-input v-model="post.body" class="input" type="text" placeholder="Описание"/>
       
              <my-button @click="createPost">Создать</my-button>
            </form>
                      
        </div>
</template>
<script>

export default {

    data() {
        return {
            post: {
                id: 0,
                title: "",
                body: ""
            },

        }
    }, methods: {
        createPost(event) {
            console.log("asdasd")
            this.post.id = Date.now();
            this.$emit('create', this.post, "govno", "govno")
            this.post = {
                title: "",
                body: ""
            }
        }
    },
}
</script>
<style scoped>
form {
    display: flex;
    flex-direction: column;
}
</style>