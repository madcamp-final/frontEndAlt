<template>
  <div class="container">
    <div class="image-container"><ImageInput /></div>
    <div class="selector-container"><OptionSelector /></div>
  </div>
</template>

<script>
import ImageInput from "../components/ImageInput.vue";
import OptionSelector from "../components/OptionSelector.vue";

export default {
  components: {
    ImageInput,
    OptionSelector,
  },
};
</script>

<style scoped>
.container {
  margin-left: 50px;
  padding-top: 30px;
}
.selector-container {
  padding-top: 30px;
}
</style>
