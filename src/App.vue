<template>
  <div>
    <carousel>
      <carousel-slide v-for="n in slides" :index="n - 1">
        <div style="position:absolute; left:0; right: 0; text-align:center; top: 50%; color: #FFF; font-size:16px;">Slide {{ n }}</div>
        <img :src="'https://picsum.photos/id/' + n + '/630/300'" width="100%">
      </carousel-slide>
    </carousel>
    <button @click="addSlide">Ajouter un slide</button>
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
    addSlide() {
      this.slides++
    }
  },
  components: {
    Carousel,
    CarouselSlide
  }
}
</script>

