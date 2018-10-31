<template>
  <section class="container h-100 position-relative">
    <div class="row h-100 z-index-10">
      <div class="col-12  my-auto">
        <div class="content-wrapper align-self-center">
          <b-carousel
            class="vert"
            id="carousel1"
            controls
            indicators
            :interval="0"
            v-model="slide"
          >

            <b-carousel-slide>
              <div class="carousel-item-inner">
                <img src="https://picsum.photos/1024/480/?image=52">
              </div>
            </b-carousel-slide>
            <b-carousel-slide>
              <div class="carousel-item-inner">
                <img src="https://picsum.photos/1024/480/?image=52">
              </div>
            </b-carousel-slide>
            <b-carousel-slide>
              <div class="carousel-item-inner">
                <img src="https://picsum.photos/1024/480/?image=52">
              </div>
            </b-carousel-slide>

           
          </b-carousel>
        </div>
      </div>
    </div>
  </section>
</template>
<style lang="scss">
.carousel {
  height: 90vh;

  .carousel-inner {
    height: inherit;

    .carousel-item {
      position:relative;
      .carousel-item-inner {
        position: absolute; 
        top: 50%;
        left: 0;
        width: 100%;
        transform:translate(-50%);
      }
    }
  }
}

.carousel-item {
  opacity: 1;
  transition-duration: .6s;
  transition-property: all;
}

.vert .carousel-item-next.carousel-item-left,
.vert .carousel-item-prev.carousel-item-right {
  -webkit-transform: translate3d(0, 0, 0);
  transform: translate3d(0, 0, 0);
  opacity: 1;
}

.vert .carousel-item-next,
.vert .active.carousel-item-right {
  -webkit-transform: translate3d(0, 100%, 0);
  transform: translate3d(0, 100% 0);
  opacity: 0;
}

.vert .carousel-item-prev,
.vert .active.carousel-item-left {
-webkit-transform: translate3d(0,-100%, 0);
        transform: translate3d(0,-100%, 0);
        opacity: 0;
}

</style>

<script>

export default {
  components: {
    
  },
  data () {
    return {
     
    }
  }
}
</script>
