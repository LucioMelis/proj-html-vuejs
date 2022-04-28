<template>
  <footer>
    <!-- Sezione top Footer -->
    <div class="footer-top">
      <div class="container container-flex">
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
            <button class="btn-trasparent">GET IN TOUCH</button>
          </div>
        </div>
        <div class="container-footer-link">
          <CardFooter
            v-for="(info, index) in ArrayInfo"
            :key="index"
            :info="info"
          />
        </div>
      </div>
    </div>
    <!-- Sezione Bottom Footer  -->
    <div class="footer-bottom">
      <a href="#header"
        ><font-awesome-icon class="icon icon-up" icon="fa-solid fa-arrow-up"
      /></a>

      <div class="container container-copy">
        <p>Enjoy the low price. We are tracking any intention of piracy.</p>
        <p>&copy; 2020 NEXGEN is Proudly Powered by <span>Codings</span></p>
      </div>
    </div>
  </footer>
</template>

<script>
import CardFooter from "@/components/CardFooter.vue";
import ArrayInfo from "@/assets/data-json/link.json";
export default {
  name: "FooterComponent",
  data() {
    return {
      ArrayInfo,
    };
  },
  components: {
    CardFooter,
  },
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
    & div:last-child {
      padding-top: 20px;
    }
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
    display: flex;
    flex-wrap: wrap;
    justify-content: space-between;
    column-gap: 10px;
  }
}
.footer-bottom {
  background-color: black;
  color: $color-text;
  position: relative;
  & p {
    font-size: 12px;
    padding: 25px 0;
  }
}
a {
  color: $color-text;
  margin-left: 10px;
}
.container-flex {
  display: flex;
}
.container-copy {
  display: flex;
  justify-content: space-between;
  span {
    color: $bg-button;
  }
}
.icon-up {
  background-color: #29292d;
  color: black;
  padding: 10px 13px;
  border-radius: 50%;
  position: absolute;
  bottom: 15px;
  right: 5px;
}
</style>
