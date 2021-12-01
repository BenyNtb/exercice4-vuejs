<template>
   <div>
    <b-carousel
      id="carousel-1"
      v-model="slide"
      data-interval="false"
      controls
      indicators
      background="#ababab"
      img-width="500"
      img-height="280"
      style="text-shadow: 1px 1px 2px #444;"
      @sliding-start="onSlideStart"
      @sliding-end="onSlideEnd"
    >
      <!-- Text slides with image -->
      <b-carousel-slide
        img-src="https://i.pinimg.com/originals/f9/11/d3/f911d38579709636499618b6b3d9b6f6.jpg"
      >
      <img src="./assets/image-tanya.jpg" alt="tanya">
      <Carousel para="I've been interested in coding for a whilr but never taken the jump, until now. I couldn't recommend this course enough. I'm now in the job of my dreams and so excited about the future.."/>
      <Carousel name="Tanya Sinclair"/>
      <Carousel job="UX Engineer"/>
  </b-carousel-slide>
      <!-- Slides with custom text -->
      <b-carousel-slide img-src="https://i.pinimg.com/originals/f9/11/d3/f911d38579709636499618b6b3d9b6f6.jpg">
         <img src="./assets/image-john.jpg" alt="tanya">
      <Carousel name="If you want to lay the best foundation possible I'd recommend taking this course. The depth the instructors go into is incredible. I now feel so confident about starting up as a professional developer"/>
      <Carousel name="John Tarkpor"/>
      <Carousel job="Junior Front-end Developer"/>
      </b-carousel-slide>

    </b-carousel>
  </div>



</template>

<script>
  import Carousel from './components/Carousel.vue'
  export default {
    components: {
      Carousel
    },
    data() {
      return {
        slide: 0,
        sliding: null,
      }
    },
    methods: {
      onSlideStart() {
        this.sliding = true
      },
      onSlideEnd() {
        this.sliding = false
      }
    }
  }
</script>

<style>
  @import url('https://fonts.googleapis.com/css2?family=Inter:wght@100&family=Manrope:wght@200&display=swap');

  * {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
    font-family: 'Inter', sans-serif;
  }

  #main {
    display: flex;
    flex-direction: row-reverse;
  }
  
</style>