<template>
  <div class="container-card-footer">
    <div class="content-card">
      <h3>About</h3>
      <ul>
        <li>
          <font-awesome-icon icon="fa-solid fa-angle-right" />
          <a href="#">Ciao</a>
        </li>
        <li>
          <font-awesome-icon icon="fa-solid fa-angle-right" />
          <a href="#">Ciao</a>
        </li>
        <li>
          <font-awesome-icon icon="fa-solid fa-angle-right" />
          <a href="#">Ciao</a>
        </li>
        <li>
          <font-awesome-icon icon="fa-solid fa-angle-right" />
          <a href="#">Ciao</a>
        </li>
        <li>
          <font-awesome-icon icon="fa-solid fa-angle-right" />
          <a href="#">Ciao</a>
        </li>
        <li>
          <font-awesome-icon icon="fa-solid fa-angle-right" />
          <a href="#">Ciao</a>
        </li>
      </ul>
    </div>
  </div>
</template>

<script>
export default {
  name: "CardFooter",
};
</script>

<style lang="scss" scoped>
@import "@/assets/style/variabili.scss";
.container-card-footer {
  background-color: #19191f;
  border-radius: 15px;
  width: calc(100% / 3);
  .content-card {
    padding: 30px;
    h3 {
      font-weight: 600;
      padding-bottom: 15px;
    }
    li {
      list-style-type: none;
      padding-top: 8px;
    }
  }
}
a {
  color: $color-text;
  margin-left: 5px;
}
</style>