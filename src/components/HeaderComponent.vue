<template>
  <header>
    <!-- ****** Header Top Hours/Info ****** -->
    <div class="header-top">
      <div class="container content-info">
        <!-- Orario apertura  -->
        <div>
          <font-awesome-icon icon="fa-solid fa-clock" />
          <span>Open Hours: Mon - Sat - 9:00 - 18:00</span>
        </div>
        <!--Container Link utili -->
        <div class="link-header">
          <div>
            <font-awesome-icon icon="fa-solid fa-phone" />
            <span><a href="#">+1(305) 1234-5678</a></span>
          </div>
          <div>
            <font-awesome-icon icon="fa-solid fa-envelope" />
            <span><a href="#">hello@example.com</a></span>
          </div>
          <font-awesome-icon icon="fa-brands fa-facebook-f" />
          <font-awesome-icon icon="fa-brands fa-twitter" />
          <font-awesome-icon icon="fa-brands fa-linkedin-in" />
        </div>
      </div>
    </div>
    <!-- ****** Header Nav-Bar  ****** -->
    <nav></nav>
  </header>
</template>

<script>
export default {
  name: "HeaderComponent",
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
@import "@/assets/style/variabili.scss";
.header-top {
  background-color: $bg-header;
  padding: 15px 0;
  & * {
    color: $color-text;
    font-size: 12px;
  }
  .content-info {
    display: flex;
    justify-content: space-between;
    align-items: center;
    span {
      margin-left: 5px;
    }
    .link-header {
      display: flex;
      column-gap: 20px;
    }
  }
}
</style>
