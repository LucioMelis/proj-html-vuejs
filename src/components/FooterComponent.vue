<template>
  <footer>
    <!-- Sezione top Footer -->
    <div class="footer-top">
      <div class="container">
        <div class="container-footer-info">
          <div class="img-logo">
            <img src="@/assets/img/logo.svg" alt="logoNextgen" />
          </div>
          <p>A Functional HTML Template for Corporate &#38; Business.</p>
          <div>
            <font-awesome-icon class="icon" icon="fa-solid fa-phone" />
            <span><a href="#">+1(305) 1234-5678</a></span>
          </div>
          <div>
            <font-awesome-icon class="icon" icon="fa-solid fa-envelope" />
            <span><a href="#">hello@example.com</a></span>
          </div>
          <div>
            <font-awesome-icon icon="fa-solid fa-location-dot" />
            <span><a href="#">Main Avenue, 987</a></span>
          </div>
          <div>
            <button @click="goToGoogleMaps" class="btn-trasparent">
              VIEW MAP
            </button>
          </div>
        </div>
        <div class="container-footer-link"></div>
      </div>
    </div>
    <!-- Sezione Bottom Footer  -->
    <div class="footer-bottom"></div>
  </footer>
</template>

<script>
export default {
  name: "FooterComponent",
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
@import "@/assets/style/variabili.scss";
.footer-top {
  padding: $padding-section;
  background-color: $bg-dark;
  color: $color-text;
  .container-footer-info {
    width: 30%;
    display: flex;
    flex-direction: column;
    row-gap: 15px;
    .img-logo {
      width: 150px;
      img {
        width: 100%;
      }
    }
    p {
      max-width: 250px;
    }
  }
  .container-footer-link {
    width: 70%;
  }
}
a {
  color: $color-text;
  margin-left: 10px;
}
</style>
