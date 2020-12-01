<template>
  <div>
    <carousel>

      <carousel-slide>
        <div style="position:absolute; left:0; right: 0; text-align:center; top: 50%; color: #FFF; font-size:16px;">  salut les gens </div>
        <img src="https://picsum.photos/id/1/630/300" width="100%">
      </carousel-slide>

      <carousel-slide>
      <div style="position:absolute; left:0; right: 0; text-align:center; top: 50%; color: #FFF; font-size:16px;"> au revoir les gens </div>
        <img src="https://picsum.photos/id/2/630/300" width="100%">
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

