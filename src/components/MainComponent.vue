<template>
  <div>
    <!-- Sezione Who We Are - Vehicle Types  -->
    <WhoWeAre />
  </div>
</template>

<script>
import WhoWeAre from "@/components/WhoWheAre.vue";

export default {
  name: "MainComponent",
  components: {
    WhoWeAre,
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
</style>
