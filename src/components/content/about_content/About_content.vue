<template>
  <div class="container my-5 about-us">
    <div class="row">
      <div class="col-md-6 p-4 p-sm-5 order-2 order-sm-1">
        <small class="text-uppercase span">About us</small>
        <h1 class="h2 mb-4 title">Lorem Ipsum <span class="span">DOLOR!</span></h1>
        <p class="text-secondary text">{{ lorem }}</p>
      </div>
      <div class="col-md-6 p-0 text-center order-1 order-sm-2">
        <img :src="image1" class="w-100" alt="slika1">
      </div>

      <div class="col-md-6 p-0 text-center">
        <img :src="image2" class="w-100" alt="slika2">
      </div>
      <div class="col-md-6 p-4 p-sm-5">
        <small class="text-uppercase span">About us</small>
        <h1 class="h2 mb-4 title">Lorem Ipsum <span class="span">DOLOR!</span></h1>
        <p class="text-secondary text">{{ lorem }}</p>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "About_content",
  components: {},
  data() {
    return {
      image1: require('./images/slika1.jpeg'),
      image2: require('./images/slika2.jpg'),
      lorem: 'Lorem ipsum dolor sit amet consectetur adipisicing elit. Suscipit repellat iure laboriosam cum voluptatum, nam minima deserunt aut? Distinctio voluptatibus dolor quaerat quo omnis illo sequi at velit, odit quod!'
    };
  },
};
</script>

<style scoped>
.title {
  font-weight: 600;
}

.text {
  line-height: 2;
}

.span {
  color: #9B5DE5;
}
</style>
