<template>
  <div class="container">
    <Signin />
    <Signup />
    <Pay />
  </div>
</template>

<script>
import Signin from "../components/Signin.vue";
import Signup from "../components/Signup.vue";
import Pay from "../components/Pay.vue";
export default {
  components: {
    Signin,
    Signup,
    Pay,
  },
};
</script>
