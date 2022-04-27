<template>
  <section>
    <div class="container">
      <div class="title-customer">
        <p class="p-intro">CUSTOMER TESTIMONIALS</p>
        <h1>Trusted<span class="dark">Feedback</span></h1>
        <p>
          We work intensively in search of ideals that can add up in the lives
          of our customers. This is what moves us and we are grateful for the
          recognition
        </p>
      </div>
      <div class="container-testimonials">
        <div
          v-for="(item, index) in arrayTestimonials"
          :key="index"
          class="card-testimonial"
        >
          <div class="content-card">
            <div>
              <img :src="imgUrl(item.companies)" alt="logo-companies" />
            </div>
            <p>
              Lorem ipsum dolor sit amet consectetur adipisicing elit.
              Excepturi, numquam nostrum? Placeat repudiandae consectetur
              ducimus blanditiis, debitis minus odio. Consectetur animi modi
              veritatis, esse fugit totam at necessitatibus asperiores magnam?
            </p>
            <div>
              <font-awesome-icon
                class="icon-size icon-color"
                icon="fa-solid fa-quote-right"
              />
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: "CustomerTestimonials",
  data() {
    return {
      arrayTestimonials: [
        {
          companies: "logo-1.png",
          feedback:
            "Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.",
        },
        {
          companies: "logo-2.png",
          feedback:
            "Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.",
        },
        {
          companies: "logo-3.png",
          feedback:
            "Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.",
        },
        {
          companies: "logo-4.png",
          feedback:
            "Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.",
        },
        {
          companies: "logo-5.png",
          feedback:
            "Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.",
        },
      ],
    };
  },
  methods: {
    imgUrl(img) {
      return require(`@/assets/img/${img}`);
    },
  },
};
</script>

<style lang="scss" scoped>
@import "@/assets/style/variabili.scss";
section {
  background-color: $bg-dark;
  padding: $padding-section;
  .container .title-customer {
    display: flex;
    flex-direction: column;
    align-items: center;
    row-gap: 25px;
    & h1 + p {
      color: $color-text;
      max-width: 900px;
      text-align: center;
    }
  }
  .container-testimonials {
    padding-top: 30px;
    display: flex;
    flex-wrap: wrap;
    column-gap: 25px;
    row-gap: 25px;
    .card-testimonial {
      background-color: #19191f;
      border-radius: 15px;
      width: calc(100% / 3 - 25px);
      .content-card {
        padding: 30px;
        & div:first-child {
          width: 120px;
          padding-bottom: 20px;
          & + p {
            color: $color-text;
            & + div {
              text-align: right;
              .icon-color {
                color: $color-text;
              }
            }
          }
          img {
            width: 100%;
            filter: invert(100%);
          }
        }
      }
    }
  }
}

h1 {
  font-size: $font-size-title;
  color: white;
  span {
    margin-left: 10px;
  }
}
</style>