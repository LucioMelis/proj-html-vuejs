<template>
  <div class="card">
    <div class="content-card">
      <div class="icon-card">
        <div>
          <font-awesome-icon
            class="icon-size"
            :icon="['fa-solid', serviceType.icon]"
          />
        </div>
        <div class="icon-arrow">
          <font-awesome-icon icon="fa-solid fa-arrow-right" />
        </div>
      </div>
      <h3>{{ serviceType.title }}</h3>
      <p>
        {{ serviceType.description }}
      </p>
    </div>
  </div>
</template>

<script>
export default {
  name: "CardServices",
  props: {
    serviceType: Object,
  },
};
</script>

<style lang="scss" scoped>
@import "@/assets/style/variabili.scss";
.card {
  background-color: #19191f;
  border-radius: 15px;
  width: calc(100% / 3 - 25px);
  &:hover {
    outline: 1px solid $bg-button;
    outline-offset: 2px;
  }
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
    }
  }
  h3 {
    color: white;
    font-weight: $font-strong;
  }
  p {
    color: $color-text;
  }
  .icon-arrow:hover {
    cursor: pointer;
    &:active {
      font-size: 10px;
    }
  }
}
</style>