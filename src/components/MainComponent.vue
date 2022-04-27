<template>
  <div>
    <!-- Sezione Who We Are - Vehicle Types  -->
    <WhoWeAre :vehicleTypes="vehicleTypes" />
    <MainServices :services="services" />
  </div>
</template>

<script>
// Componenti Main
import WhoWeAre from "@/components/WhoWheAre.vue";
import MainServices from "@/components/MainServices.vue";
// Data Main
import vehicleTypes from "@/assets/data-json/vehicle-types";
import services from "@/assets/data-json/services";

export default {
  name: "MainComponent",
  data() {
    return {
      vehicleTypes,
      services,
    };
  },
  components: {
    WhoWeAre,
    MainServices,
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
</style>
