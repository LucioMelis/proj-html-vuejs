<template>
  <div class="card">
    <div class="content-card">
      <div class="icon-card">
        <div>
          <font-awesome-icon
            class="icon-size"
            icon="fa-solid fa-truck-ramp-box"
          />
        </div>
        <div>
          <font-awesome-icon icon="fa-solid fa-arrow-right" />
        </div>
      </div>
      <h3>Tecnology</h3>
      <p>
        Lorem ipsum dolor sit amet consectetur adipisicing elit. Aliquam minima
        aperiam debitis velit nostrum placeat veritatis numquam deserunt
        delectus nulla illum eum, doloremque hic voluptates repellat obcaecati
        unde voluptatum neque?
      </p>
    </div>
  </div>
</template>

<script>
export default {
  name: "CardServices",
};
</script>

<style lang="scss" scoped>
@import "@/assets/style/variabili.scss";
.card {
  background-color: #19191f;
  border-radius: 15px;
}
.content-card {
  padding: 30px;
  & > * {
    padding-bottom: 20px;
  }
  .icon-card {
    color: $bg-button;
    display: flex;
    justify-content: space-between;
    & div:first-child {
      background-color: $bg-title-dark;
      padding: 10px;
      border-radius: 50%;
      .icon-size {
        font-size: 25px;
      }
    }
  }
  h3 {
    color: white;
    font-weight: $font-strong;
  }
  p {
    color: $color-text;
  }
}
</style>