<template>
  <div class="container-card-footer">
    <div class="content-card">
      <h3>{{ info.title }}</h3>
      <ul>
        <li v-for="(link, index) in info.link" :key="index">
          <font-awesome-icon icon="fa-solid fa-angle-right" />
          <a href="#">{{ link }}</a>
        </li>
      </ul>
    </div>
  </div>
</template>

<script>
export default {
  name: "CardFooter",
  props: {
    info: Object,
  },
};
</script>

<style lang="scss" scoped>
@import "@/assets/style/variabili.scss";
.container-card-footer {
  background-color: #19191f;
  border-radius: 5px;
  width: calc(100% / 3 - 10px);
  .content-card {
    padding: 30px;
    h3 {
      font-weight: 600;
      padding-bottom: 15px;
      color: white;
    }
    li {
      list-style-type: none;
      padding-top: 8px;
    }
  }
}
a {
  color: $color-text;
  margin-left: 12px;
}
</style>