<template>
  <div class="global-nav-bar">
    <GlobalNavBar />
  </div>
</template>

<script>
import GlobalNavBar from "./components/GlobalNavBar.vue";

export default {
  name: "App",
  components: {
    GlobalNavBar,
  },
};
</script>

<style>
@import url("https://fonts.googleapis.com/css?family=Roboto:100,300,400,700&display=swap");

* {
  font-family: "Apple SD Gothic Neo", Roboto, "Noto Sans KR", NanumGothic,
    "Malgun Gothic", sans-serif;
  margin: 0;
  padding: 0;
  border: 0;
  line-height: 1.2;
  word-wrap: break-word;
  box-sizing: border-box;
  list-style: none;
  color: rgb(29, 29, 31);
  text-decoration: none;
  -webkit-font-smoothing: antialiased;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
}
table {
  border-collapse: collapse;
  border-spacing: 0;
}
img {
  max-width: 100%;
  height: auto;
  border: 0;
}
button {
  border: 0;
  cursor: pointer;
}
</style>
