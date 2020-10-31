<template>
    <section class="blog" v-if="blog.length >0" >
        <div class="stories_container">
            <h2 class="section_header">Trending stories</h2>
            <a class="btn_view">View all > </a>
        </div>
        <div class="blog_blocks_wrapper">
            <div class="bl_container" v-for="element in blog" :key="element.name">
                <img :src="element.image" alt="blog_picture">
                <div class="blog_text_wrapper">
                    <p class="blog_name">{{element.name}}</p>
                    <p class="article_part">{{element.article}}</p>
                    <a class="read_btn">Read more</a>
                </div>
            </div>
        </div>
    </section>
</template>

<script>
    export default {
        name: "Blog",
        data: function () {
            return {
                blog: [

                ],

                index: 0,

            }
        },

        mounted() {
            fetch("api/blog.json").then(function(response) {
                return response.json()
            }).then((response)=> {
                this.blog= response
            })
        }
    }

</script>

<style scoped>

</style>