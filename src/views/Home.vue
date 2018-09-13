<template>
  <div class="home">
    <img alt="Vue logo" src="../assets/logo.png">
    <HelloWorld msg="Welcome to Your Vue.js App"/>
  </div>
</template>

<script>
// @ is an alias to /src
import HelloWorld from "@/components/HelloWorld.vue";

export default {
  name: "home",
  created() {
    if (window.Stripe === undefined) {
      this.$swal("Hello", "Stripe is not loaded", "error");
    } else {
      this.$swal("Hello", "Stripe is loaded", "success");
    }
  },
  components: {
    HelloWorld
  }
};
</script>
