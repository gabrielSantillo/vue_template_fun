<template>
    <div>
        <h1>{{ blog_title }}</h1>
        <p>{{ blog_content }}</p>
        <img :src="blog_img_url" alt="">
    </div>
</template>

<script>
    export default {
        data() {
            return {
                blog_content: `Content blog.`,
                blog_title: `Blog Title`,
                blog_img_url: `https://images.pexels.com/photos/39317/chihuahua-dog-puppy-cute-39317.jpeg?auto=compress&cs=tinysrgb&w=1260&h=750&dpr=1`
            }
        },
    }
</script>

<style scoped>

</style>