<template>
  <div>
    <carousel>

      <carousel-slide>
        salut les gens
        <img src="https://picsum.photos/id/1/630/300">
      </carousel-slide>

      <carousel-slide>
        au revoir les gens
        <img src="https://picsum.photos/id/2/630/300">
      </carousel-slide>
    </carousel>

  </div>
</template>

<script>
import Carousel from './components/carousel/Carousel'
import CarouselSlide from './components/carousel/CarouselSlide'

export default {
  data () {
    return {
      slides: 5,
      
    }
  },
  methods: {
    
  },
  components: {
    Carousel,
    CarouselSlide
  }
}
</script>

