<template>
  <div>
    <!-- Sezione Who We Are - Vehicle Types  -->
    <WhoWeAre :vehicleTypes="vehicleTypes" />
    <MainServices :services="services" />
    <LogisticalProcedure :logistical="logistical" />
  </div>
</template>

<script>
// Componenti Main
import WhoWeAre from "@/components/WhoWheAre.vue";
import MainServices from "@/components/MainServices.vue";
import LogisticalProcedure from "@/components/LogisticalProcedure.vue";
// Data Main
import vehicleTypes from "@/assets/data-json/vehicle-types";
import services from "@/assets/data-json/services";
import logistical from "@/assets/data-json/logistical-procedure";

export default {
  name: "MainComponent",
  data() {
    return {
      vehicleTypes,
      services,
      logistical,
    };
  },
  components: {
    WhoWeAre,
    MainServices,
    LogisticalProcedure,
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
</style>
