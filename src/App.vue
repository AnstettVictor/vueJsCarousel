<template>
  <div>
    <carousel>

      <carousel-slide>
        salut les gens
      </carousel-slide>

      <carousel-slide>
        au revoir les gens
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

