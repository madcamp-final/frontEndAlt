<template>
  <dropdown
    class="my-dropdown-toggle"
    :options="keywords"
    :selected="object"
    v-on:updateOption="methodToRunOnSelect"
    :placeholder="'Select an Item'"
    :closeOnOutsideClick="boolean"
  >
  </dropdown>
</template>

<script>
import dropdown from "vue-dropdowns";

export default {
  props: {
    keywords: [Array, Object],
  },
  data() {
    return {
      object: {},
    };
  },

  components: {
    dropdown: dropdown,
  },

  methods: {
    methodToRunOnSelect(payload) {
      this.object = payload;
    },
  },
};
</script>

<style scoped>
.my-dropdown-toggle {
  border-radius: 5px;
}
</style>
