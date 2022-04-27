<template>
  <header>
    <!-- ****** Header Top Hours/Info ****** -->
    <div class="header-top">
      <div class="container content-info">
        <!-- Orario apertura  -->
        <div>
          <font-awesome-icon class="icon" icon="fa-solid fa-clock" />
          <span>Open Hours: Mon - Sat - 9:00 - 18:00</span>
        </div>
        <!--Container Link utili -->
        <div class="link-header">
          <div>
            <font-awesome-icon class="icon" icon="fa-solid fa-phone" />
            <span><a href="#">+1(305) 1234-5678</a></span>
          </div>
          <div>
            <font-awesome-icon class="icon" icon="fa-solid fa-envelope" />
            <span><a href="#">hello@example.com</a></span>
          </div>
          <font-awesome-icon class="icon" icon="fa-brands fa-facebook-f" />
          <font-awesome-icon class="icon" icon="fa-brands fa-twitter" />
          <font-awesome-icon class="icon" icon="fa-brands fa-linkedin-in" />
        </div>
      </div>
    </div>
    <!-- ****** Header Nav-Bar  ****** -->
    <nav class="container content-nav">
      <!-- contenitore immagine  -->
      <div class="container-logo">
        <img src="@/assets/img/logo.svg" alt="logoNextgen" />
      </div>
      <!-- contenitore link nav-bar  -->
      <div class="container-nav">
        <ul>
          <li v-for="element in menuNav" :key="element">
            <a href="#">{{ element }}</a>
          </li>
        </ul>
        <div>
          <font-awesome-icon class="icon" icon="fa-regular fa-user" />
        </div>
        <div>
          <button class="btn btn-header">GET IN TOUCH</button>
        </div>
      </div>
    </nav>
    <!-- ****** Sezione Jumbotron  ****** -->
    <div class="container">
      <div class="jumbotron">
        <p>LOGISTICS SERVICES</p>
        <h1>CARGO TRANSPORT</h1>
        <p class="description">
          Fractional or exclusive road cargo transportation to all regions,with
          small,medium and large vehicles.
        </p>
        <p v-if="showMore" class="description">
          Lorem ipsum dolor sit amet consectetur adipisicing elit. Inventore ex
          nihil culpa, dicta quisquam accusantium optio consequatur aspernatur
          vitae earum cumque quidem expedita nobis, quasi repellendus! Minima
          blanditiis doloremque obcaecati. Lorem ipsum dolor sit, amet
          consectetur adipisicing elit. Quo adipisci saepe ipsam dolore, minus
          officia sapiente excepturi sequi, nemo similique vel voluptatum
          dignissimos nostrum nihil quibusdam ab rem maiores labore.
        </p>
        <div>
          <button class="btn-header">GET IN TOUCH</button>
          <button @click="readMore" class="btn-trasparent">READ MORE</button>
        </div>
      </div>
    </div>
  </header>
</template>

<script>
export default {
  name: "HeaderComponent",
  data() {
    return {
      menuNav: ["HOME", "ABOUT", "SERVICES", "PROCESS", "TESTIMONIALS"],
      showMore: false,
    };
  },
  methods: {
    readMore() {
      this.showMore = !this.showMore;
    },
  },
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
.content-nav {
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 10px 0;
  .container-logo {
    width: 150px;
    img {
      width: 100%;
    }
  }
  .container-nav {
    display: flex;
    align-items: center;
    column-gap: 20px;
    & * {
      color: white;
    }
    & ul {
      display: flex;
      align-items: center;
      column-gap: 20px;
      font-weight: $font-strong;
    }
    & ul li {
      list-style-type: none;
    }
  }
}

.jumbotron {
  padding-top: 130px;
  padding-bottom: 150px;
  max-width: 500px;
  & p:first-child {
    color: $color-text-p;
    font-weight: $font-lighter;
  }
  & div {
    display: flex;
    column-gap: 20px;
  }
  h1 {
    font-size: 80px;
    color: white;
    font-weight: $font-bold;
  }
  .description {
    color: $color-text;
    padding-bottom: 30px;
  }
}
</style>
