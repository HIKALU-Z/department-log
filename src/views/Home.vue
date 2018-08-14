<template>
  <div>
    <Nav></Nav>
    <div class="container">
      <Log></Log>
    </div>
  </div>
</template>

<script>
import Nav from "@/components/Nav";
// @ is an alias to /src
import Log from "@/components/Log.vue";

export default {
  name: "home",
  components: {
    Nav,
    Log
  }
};
</script>

<style lang="scss" scoped>
.container {
  padding: 20px 0;
}
</style>
