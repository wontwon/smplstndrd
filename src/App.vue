<template>
  <nav-bar></nav-bar>
    <div class="row center">
      <div class="section">
        <h5 class="white-text marketing-header">Tsukue 
机 v1.0</h5>
        <p class="white-text marketing-text">Simple. Strong. Standing Portable Desk. $99. </p>
        <p class="white-text marketing-text">Ships 06/2016</p>
        <div class="section">
          <button data-celery="5706bf3f07160b1100ebf36d" class="waves-effect waves-light btn light-green accent-3 white-text">Pre-Order Now</button>
        </div>
      </div>
    </div>
    <div class="current-image-box">
      <div class="animated fadeInUp" v-if="currentImage === 'background'">
        <img class="responsive-img" src="./assets/background.jpg" alt="">      
      </div>
      <div class="animated fadeInUp" v-if="currentImage === 'folded'">
        <img class="responsive-img" src="./assets/folded.jpg" alt="">      
      </div>
      <div class="animated fadeInUp" v-if="currentImage === 'spread'">
        <img class="responsive-img" src="./assets/spread.jpg" alt="">      
      </div>
      <div class="animated fadeInUp" v-if="currentImage === 'front'">
        <img class="responsive-img" src="./assets/front.jpg" alt="">      
      </div>
      <div class="animated fadeInUp" v-if="currentImage === 'back'">
        <img class="responsive-img" src="./assets/back.jpg" alt="">      
      </div>
      <div class="animated fadeInUp" v-if="currentImage === 'side'">
        <img class="responsive-img" src="./assets/side.jpg" alt="">      
      </div>
      <div class="animated fadeInUp" v-if="currentImage === 'top'">
        <img class="responsive-img" src="./assets/top.jpg" alt="">      
      </div>
      <div class="animated fadeInUp" v-if="currentImage === 'full'">
        <img class="responsive-img" src="./assets/full.jpg" alt="">      
      </div>
    </div>


    <div class="row z-depth-1 hide-on-small-only animated slideInUp">
      <div @click="handleImageClick('folded')" id="image-1" class="col l3  m3 s6"></div>
      <div @click="handleImageClick('spread')" id="image-2" class="col l3  m3 s6"></div>
      <div @click="handleImageClick('front')" id="image-3" class="col l3  m3 s6"></div>
      <div @click="handleImageClick('back')" id="image-4" class="col l3  m3 s6"></div>
      <div @click="handleImageClick('side')" id="image-5" class="col l3  m3 s6"></div>
      <div @click="handleImageClick('top')" id="image-6" class="col l3  m3 s6"></div>
      <div @click="handleImageClick('full')" id="image-7" class="col l3  m3 s6"></div>
      <div @click="handleImageClick('background')" id="image-8" class="col l3  m3 s6"></div>
    </div>
  </div>

  <div class="row z-depth-1 hide-on-med-and-up animated slideInUp">
      <div @click="handleImageClick('folded')" id="image-1" class="col s3 image-small"></div>
      <div @click="handleImageClick('spread')" id="image-2" class="col s3 image-small"></div>
      <div @click="handleImageClick('front')" id="image-3" class="col s3 image-small"></div>
      <div @click="handleImageClick('back')" id="image-4" class="col s3 image-small"></div>
      <div @click="handleImageClick('side')" id="image-5" class="col s3 image-small"></div>
      <div @click="handleImageClick('top')" id="image-6" class="col s3 image-small"></div>
      <div @click="handleImageClick('full')" id="image-7" class="col s3 image-small"></div>
      <div @click="handleImageClick('background')" id="image-8" class="col s3 image-small"></div>
    </div>

  <div class="row center">
    <h3 class="white-text">[$99] </h3>
    <a data-celery="5706bf3f07160b1100ebf36d" class="waves-effect waves-light btn light-green accent-3 white-text">Pre-Order 
    Now</a>
    <p class="white-text marketing-text">Ships 06/2016</p>
  </div>

  <materials-overview></materials-overview>
  <page-footer></page-footer>
</template>

<script>
  import NavBar from './components/NavBar'
  import MaterialsOverview from './components/MaterialsOverview'
  import PageFooter from './components/PageFooter'

  import $ from 'jquery'
  import 'materialize-css/bin/materialize.js'


  export default {
    components: {
      NavBar,
      MaterialsOverview,
      PageFooter
    },
    data() {
      return {
        currentImage: 'background'
      }
    },
    methods: {
      handleImageClick(image){
        this.currentImage = image
      }
    }
  }

</script>


<style>

  html {
    height: 100%;
    background-color: black;,
    font-family: GillSans, Calibri, Trebuchet, sans-serif;
  }

  .animated {
    animation-duration: 0.4s;
    -webkit-animation-duration: 0.4s;
    -moz-animation-duration: 0.4s;
  }

  .preorder-button {
    position: absolute;
    padding: 20px 10px;
    right: 0;
  }

  .marketing-header {
    margin: 0px;
  }

  .marketing-text {
    margin: 0px;
  }


  .image-small {
    max-height: 100px;
  }

  #image-1 {
    height: 200px;
    background-size: cover;
    background-image: url('./assets/folded.jpg')
  }

  #image-2 {
    height: 200px;
    background-size: cover;
    background-image: url('./assets/spread.jpg')
  }

  #image-3 {
    height: 200px;
    background-size: cover;
    background-image: url('./assets/front.jpg')
  }

  #image-4 {
    height: 200px;
    background-size: cover;
    background-image: url('./assets/back.jpg')
  }

  #image-5 {
    height: 200px;
    background-size: cover;
    background-image: url('./assets/side.jpg')
  }

  #image-6 {
    height: 200px;
    background-size: cover;
    background-image: url('./assets/top.jpg')
  }

  #image-7 {
    height: 200px;
    background-size: cover;
    background-image: url('./assets/full.jpg')
  }

  #image-8 {
    height: 200px;
    background-size: cover;
    background-image: url('./assets/background.jpg')
}

</style>
