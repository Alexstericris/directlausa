<template>
  <div class="hello">
      <b-carousel
          id="carousel-1"
          fade
          v-model="slide"
          controls
          indicators
          background="#ababab"
          img-width="1024"
          img-height="480"
          style="text-shadow: 1px 1px 2px #333;"
      >
          <!-- Text slides with image -->
          <b-carousel-slide class="my-carousel-slide"
              caption="First slide"
              text="Nulla vitae elit libero, a pharetra augue mollis interdum.">
              <template #img>
                  <img
                      class="d-block img-fluid w-100"
                      width="1024"
                      height="480"
                      src="../assets/lemons.jpeg"
                      alt="image slot"
                  >
              </template>
          </b-carousel-slide>

          <!-- Slides with custom text -->
          <b-carousel-slide class="my-carousel-slide">
              <template #img>
                  <img
                      class="d-block img-fluid w-100"
                      width="1024"
                      height="480"
                      src="../assets/pages.jpeg"
                      alt="image slot"
                  >
              </template>
              <h1>Hello world!</h1>
          </b-carousel-slide>

          <!-- Slides with image only -->
          <b-carousel-slide class="my-carousel-slide">
              <template #img>
                  <img
                      class="d-block img-fluid w-100"
                      width="1024"
                      height="480"
                      src="../assets/salad.jpeg"
                      alt="image slot"
                  >
              </template>
          </b-carousel-slide>

          <!-- Slides with img slot -->
          <!-- Note the classes .d-block and .img-fluid to prevent browser default image alignment -->
          <b-carousel-slide class="my-carousel-slide">
              <template #img>
                  <img
                      class="d-block img-fluid w-100"
                      width="1024"
                      height="480"
                      src="../assets/lemons.jpeg"
                      alt="image slot"
                  >
              </template>
          </b-carousel-slide>

          <!-- Slide with blank fluid image to maintain slide aspect ratio -->
          <b-carousel-slide class="my-carousel-slide" caption="Blank Image" img-blank img-alt="Blank image">
              <p>
                  Lorem ipsum dolor sit amet, consectetur adipiscing elit. Suspendisse eros felis, tincidunt
                  a tincidunt eget, convallis vel est. Ut pellentesque ut lacus vel interdum.
              </p>
          </b-carousel-slide>
      </b-carousel>
  </div>
</template>

<script>
import '../assets/lemons.jpeg'
export default {
    name: 'HelloWorld',
    props: {
        msg: String
    },
    data() {
        return {
            slide: 0,
            sliding: null
        }
    },
    methods: {
        onSlideStart(slide) {
            this.sliding = true
        },
        onSlideEnd(slide) {
            this.sliding = false
        }
    }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
#carousel-1{
    z-index: -99;
    width: 80%;
    margin: auto;

}.my-carousel-slide{
     max-height: 800px;
     object-fit: scale-down;
}
h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>
