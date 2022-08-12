<template>
    <div>
        <button @click="changePost">Turn on/off</button>

        <section v-if="posts[0][`show_post`] === true">
            <div v-for="(post, index) in posts" :key="index">
            <p>{{ post[`blog_content`] }}</p>
            <p>{{ post[`blog_title`] }}</p>
            <img :src="post[`blog_img_url`]" alt="">
        </div>
        </section>

    </div>
</template>

<script>
    export default {

        methods: {
            changePost() {
                this.show_post = !this.show_post;
            }
        },

        data() {
            return {
                show_post : true,
                posts: [
                    {
                        blog_content: `Content blog.`,
                        blog_title: `Blog Title`,
                        blog_img_url: `https://images.pexels.com/photos/39317/chihuahua-dog-puppy-cute-39317.jpeg?auto=compress&cs=tinysrgb&w=1260&h=750&dpr=1`
                        
                    },
                    {
                        blog_content: `Content blog.`,
                        blog_title: `Blog Title`,
                        blog_img_url: `https://images.pexels.com/photos/39317/chihuahua-dog-puppy-cute-39317.jpeg?auto=compress&cs=tinysrgb&w=1260&h=750&dpr=1`
                    },
                    {
                        blog_content: `Content blog.`,
                        blog_title: `Blog Title`,
                        blog_img_url: `https://images.pexels.com/photos/39317/chihuahua-dog-puppy-cute-39317.jpeg?auto=compress&cs=tinysrgb&w=1260&h=750&dpr=1`
                    }
                
                ]

            }
        },
    }
</script>

<style scoped>

</style>