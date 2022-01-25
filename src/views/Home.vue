<template>
  <div>
    <div class="main-page">
      <MainPage />
    </div>
    <div class="footer">
      <Footer />
    </div>
  </div>
</template>

<script>
import MainPage from "../components/MainPage.vue";
import Footer from "../components/Footer.vue";

export default {
  name: "Home",
  components: {
    MainPage,
    Footer,
  },
};
</script>

<style scoped></style>
