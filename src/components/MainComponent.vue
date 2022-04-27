<template>
  <div>
    <!-- Sezione Who We Are - Vehicle Types  -->
    <WhoWeAre :vehicleTypes="vehicleTypes" />
  </div>
</template>

<script>
import WhoWeAre from "@/components/WhoWheAre.vue";
import vehicleTypes from "@/assets/data-json/vehicle-types";

export default {
  name: "MainComponent",
  data() {
    return {
      vehicleTypes,
    };
  },
  components: {
    WhoWeAre,
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
</style>
