<template>
    <section class="destinations">
        <div class="small_header">
            <h2 class="section_header">Featured destinations</h2>
            <a class="btn_view">View all > </a>
        </div>

        <div class="destination_suggestions" v-if="destinations.length >0">
            <div class="place_container" v-for="part in destinations" :key="part.picture">
                <img :src="part.picture" alt="destination_picture">
                <div class="destination_name_wrapper">
                    <div class="destination_rectangle"></div>
                    <a class="location text">{{part.location1}}</a><br>
                    <a class="country text">{{part.country1}}</a>

                </div>
            </div>
        </div>
    </section>
</template>

<script>
    export default {
        name: "Destinations",

        data: function () {
            return {
                destinations: [

                ],

                index: 0,

            }
        },

        mounted() {
            fetch("api/destinations.json").then(function(response) {
                return response.json()
            }).then((response)=> {
                this.destinations= response
            })
        }
    }


</script>

<style scoped>

</style>