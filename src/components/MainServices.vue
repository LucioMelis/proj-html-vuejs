<template>
  <section>
    <div class="container">
      <p class="p-intro">ROAD TRANSPORT</p>
      <h1>Main <span>Services</span></h1>
      <div class="intro-button">
        <p>
          With all of this expertis and capability come an unrivalled commitment
          to customer service. We will work hard to understand your needs in
          order to develop a productive, long-term partnership.
        </p>
        <div><button class="btn-trasparent">SEE ALL</button></div>
      </div>
      <div class="container-services">
        <CardServices />
      </div>
    </div>
  </section>
</template>

<script>
import CardServices from "@/components/CardServices.vue";
export default {
  name: "MainServices",
  components: {
    CardServices,
  },
  props: {
    services: Array,
  },
};
</script>

<style lang="scss" scoped>
@import "@/assets/style/variabili.scss";
section {
  background-color: $bg-dark;

  .container {
    padding: $padding-section;
    & > * {
      padding-bottom: 20px;
    }
    .intro-button {
      display: flex;
      justify-content: space-between;
    }
    h1 {
      font-size: $font-size-title;
    }
    h1,
    h3 {
      color: white;
    }
    div > p {
      color: $color-text;
      max-width: 1000px;
    }
    span {
      padding: 5px 10px;
      background-color: $bg-title-dark;
    }
    .container-services {
      padding-top: 20px;
      width: calc(100% / 3);
    }
  }
}
</style>