<template>
  <section>
    <div class="content-section">
      <!-- sezione Logistica  -->
      <div class="logistical-procedure">
        <p class="p-intro">HOW IT WORKS IN PRACTICE</p>
        <h1>
          <span class="light"> Logistical </span>
          Procedure
        </h1>
        <p class="description">
          We work width innovative methodologies to ensure that the entire
          delivery process is done from start to finish as planned
        </p>
      </div>
      <!-- Sezione Metodi  -->
      <div class="methodologies">
        <div v-for="(element, index) in logistical" :key="index" class="card">
          <p class="position">
            <span>{{ element.number }}</span>
          </p>
          <h3>{{ element.title }}</h3>
          <p class="description">
            {{ element.text }}
          </p>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: "LogisticalProcedure",
  props: {
    logistical: Array,
  },
};
</script>

<style lang="scss" scoped>
@import "@/assets/style/variabili.scss";
section {
  margin: 80px 0;
  .content-section {
    .logistical-procedure {
      text-align: center;
      padding-bottom: 30px;
      border-bottom: 5px solid $bg-title;
      & > * {
        padding-bottom: 20px;
      }
    }
    .methodologies {
      display: flex;
      justify-content: space-around;
      .card {
        width: calc(100% / 6);
        display: flex;
        flex-direction: column;
        align-items: center;
        & > * {
          padding: 5px 15px;
        }
        h3 {
          font-weight: $font-strong;
          text-align: center;
          max-width: 200px;
        }
        .position {
          position: relative;
          span {
            position: absolute;
            display: block;
            top: -180%;
            left: -2%;
            color: $color-title-p;
            background-color: $bg-title;
            padding: 5px;
            border-radius: 50%;
            font-weight: 600;
          }
        }
      }
    }
  }
}
h1 {
  font-size: $font-size-title;
}
.description {
  color: #69696d;
  text-align: center;
}
</style>