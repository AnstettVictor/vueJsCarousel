<template>
    <div class="carousel"> 
        <slot></slot>
        <button class="carousel__nav carousel__next" @click="next"></button>
        <button class="carousel__nav carousel__prev" @click="prev"></button>
    </div>
</template>

<script>
export default {
    
    data() {
       
        return {
            index: 0,
            slides: [],
            direction: null
        }
    },
    computed: {
        slidesCount() {
            return this.slides.length
        }
    },
    mounted() {
        this.slides = this.$children
        this.slides.forEach((slide, i) => {
            slide.index = i
        })
    },
    methods: {
        next () {
            this.index++
            this.direction = 'right'
            if (this.index >= this.slidesCount) {
                this.index = 0
            }
        },
        prev () {
            this.index--
            this.direction = 'left'
            if (this.index < 0) {
                this.index = this.slidesCount - 1
            }
        }
    },
}
</script>
<style>
  .carousel {
    position: relative;
    overflow: hidden;
  }

  .carousel__nav{
    position: absolute;
    top: 50%;
    margin-top:-31px;
    left: 10px;
    background: url(prev.png);
    width: 63px;
    height:63px;
  }

  .carousel__nav.carousel__next{
    right: 10px;
    left: auto;
    background-image: url(next.png);
  }

  .carousel__pagination {
    position: absolute;
    bottom: 10px;
    left: 0;
    right: 0;
    text-align: center;
  }

  .carousel__pagination button{
    display: inline-block;
    width: 10px;
    height: 10px;
    background-color: #000;
    opacity: 0.8;
    border-radius: 10px;
    margin: 0 2px;
  }

  .carousel__pagination button.active{
    background-color: #fff;
  }
</style>
