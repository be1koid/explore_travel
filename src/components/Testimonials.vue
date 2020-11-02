<template>
  <section class="testimonials">

    <div class="testim_container" v-if="testimonials.length >0">
      <h2 class="section_header testim_header">Testimonials</h2>
      <div class="five_stars">
        <img v-for="i of testimonials[index].rating" src="../assets/Star.svg" :alt="'star' + i" :key="i">
      </div>
      <p class="testimonials_text">{{testimonials[index].comment}}</p>
      <p class="edward">{{testimonials[index].name}}</p>
      <p class="founder">{{testimonials[index].position}}</p>
    </div>

    <div class="Edward_rectangle" v-if="testimonials.length >0">
      <img :src="testimonials[index].image" alt="Edward">
      <div class="switcher_edward">
        <img class="prev" src="../assets/previous_btn.svg" alt="previous" @click="counter -= 1">
        <img class="next" src="../assets/next_btn.svg" alt="next" @click="counter += 1">
      </div>
    </div>
  </section>

</template>

<script>
export default {

  name: "Testimonials",

  data: function () {
    return {
      testimonials: [

      ],

      counter: 0,

    }
  },

  computed: {
    index () {
      if ( this.counter < 0) {
        return (this.testimonials.length + (this.counter % this.testimonials.length)) % this.testimonials.length
      }
        return this.counter % this.testimonials.length
    }
  },

  mounted() {
    fetch("api/testimonials.json").then(function(response) {
      return response.json()
    }).then((response)=> {
      this.testimonials= response
    })
  }


}




</script>

<style scoped>

</style>