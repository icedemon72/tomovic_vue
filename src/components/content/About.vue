<template>
  <div>
    <Navbar />
    <About_content />
    <Footer class="footer" />
  </div>
</template>

<script>
import Navbar from "./../menu/Navbar";
import Footer from "./../footer/Footer.vue";
import About_content from "./about_content/About_content.vue";
export default {
  name: "About",
  components: { Navbar, Footer, About_content },
};
</script>
