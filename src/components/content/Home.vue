<template>
  <div>
    <Navbar />
    <h1 class="brand-text">PRODAVNICA ODECE</h1>
    <Content class="content"/>
    <Footer class="footer" />
  </div>
</template>

<script>
import Navbar from "./../menu/Navbar";
import Footer from "./../footer/Footer.vue";
import Content from "./home_content/Content";

export default {
  name: "Home",
  components: {
    Navbar,
    Footer,
    Content,
  },
};
</script>

<style>
  body {
    position: relative;
    min-height: 100vh;
  }

  .brand-text {
    text-align: center;
    font-weight: 900;
  }

  .content {
    padding-bottom: 3.5rem;    /* Footer height */
  }

  .footer {
    position: absolute;
    bottom: 0;
    width: 100%;
    height: 3.5rem;            /* Footer height */
  }

</style>
