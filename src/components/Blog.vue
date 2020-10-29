<template>
    <section class="blog" v-if="blog.length >0" >
        <div class="stories_container">
            <h2 class="section_header">Trending stories</h2>
            <a class="btn_view">View all > </a>
        </div>
        <div class="blog_blocks_wrapper">
            <div class="bl_container">
                <img :src="blog[index].image" alt="Yoga girl">
                <div class="blog_text_wrapper">
                    <p class="blog_name">{{blog[index].name}}</p>
                    <p class="article_part">{{blog[index].article}}</p>
                    <a class="read_btn">Read more</a>
                </div>
            </div>
            <div class="food_container">
                <img :src="blog[index].image" alt="Japanese food">
                <div class="blog_text_wrapper">
                    <p class="blog_name">{{blog[index].name}}</p>
                    <p class="article_part">{{blog[index].article}}</p>
                    <a class="read_btn">Read more</a>
                </div>
            </div>
            <div class="chichen_container">
                <img :src="blog[index].image" alt="Chichen Itza">
                <div class="blog_text_wrapper">
                    <p class="blog_name">{{blog[index].name}}</p>
                    <p class="article_part">{{blog[index].article}}</p>
                    <a class="read_btn">Read more</a>
                </div>
            </div>
            <div class="surf_container">
                <img :src="blog[index].image" alt="surfer">
                <div class="blog_text_wrapper">
                    <p class="blog_name">{{blog[index].name}}</p>
                    <p class="article_part">{{blog[index].article}}</p>
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