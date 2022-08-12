<template>
    <div>
        <button @click="changePost">Turn on/off</button>
        <div v-if="show_post === true">
        <h1>{{ blog_title }}</h1>
        <p>{{ blog_content }}</p>
        <img :src="blog_img_url" alt="">
        </div>
    </div>
</template>

<script>
    export default {

        methods: {
            changePost() {
                if(this.show_post === true) {
                    this.show_post = false
                } else {
                    this.show_post = true
                }
            }
        },

        data() {
            return {
                blog_content: `Content blog.`,
                blog_title: `Blog Title`,
                blog_img_url: `https://images.pexels.com/photos/39317/chihuahua-dog-puppy-cute-39317.jpeg?auto=compress&cs=tinysrgb&w=1260&h=750&dpr=1`,
                show_post : true
            }
        },
    }
</script>

<style scoped>

</style>