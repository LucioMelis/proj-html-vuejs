<template>
  <section>
    <div class="container">
      <!-- Container Who we are  -->
      <div class="container-section-general">
        <div class="exellence">
          <p>WHO WE ARE</p>
          <h1>
            <span>
              <font-awesome-icon icon="fa-regular fa-gem" />Excellence
            </span>
            in Transport
          </h1>
          <p>
            Lorem ipsum dolor sit, amet consectetur adipisicing elit. Architecto
            molestiae quo vitae totam possimus ducimus, consequatur numquam
            repellat, voluptate excepturi ex eligendi tempora voluptates eveniet
            atque quos ipsam recusandae nesciunt?
          </p>
          <p>
            Lorem ipsum dolor, sit amet consectetur adipisicing elit. Totam
            accusamus corporis illo iste nam nostrum, iure praesentium natus
            iusto rerum quia est? Dolor, expedita ea dignissimos exercitationem
            vitae assumenda. Itaque.
          </p>
          <div>
            <p class="italic">
              <i>
                Lorem ipsum dolor sit amet consectetur adipisicing elit. Itaque
                eum est maxime, enim atque aliquid nobis ipsam dignissimos.
                Nostrum culpa dolore illo doloribus minima minus earum accusamus
                deserunt ullam. Mollitia.
              </i>
            </p>
          </div>
          <p>
            Lorem ipsum dolor sit amet consectetur adipisicing elit. Quas eius
            ullam velit ab.
          </p>
          <ul>
            <li>Lorem ipsum dolor si amet con inuna oculata</li>
            <li>Lorem ipsum dolor si amet con inuna oculata</li>
            <li>Lorem ipsum dolor si amet con inuna oculata</li>
            <li>Lorem ipsum dolor si amet con inuna oculata</li>
            <li>Lorem ipsum dolor si amet con inuna oculata</li>
          </ul>
        </div>
        <!-- Container Vehicle Types  -->
        <div class="vehicle-types"></div>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: "WhoWeAre",
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
@import "@/assets/style/variabili.scss";
.container-section-general {
  display: flex;
  justify-content: space-between;
  padding: 80px 0;
  .exellence {
    width: 65%;
    h1 {
      color: black;
      font-size: 35px;
      padding-bottom: 20px;
      span {
        background-color: #daeced;
        padding: 5px 10px;
        margin-right: 5px;
        color: $bg-button;
      }
    }
    & > * {
      color: $color-text-darker;
    }
    & > p:first-child {
      color: #1aafb7;
      font-weight: $font-lighter;
    }
    & > p {
      padding-bottom: 20px;
    }
    div {
      border-left: 4px solid #daeced;
      margin-bottom: 10px;
      p {
        padding: 10px 0 10px 20px;
      }
    }
    li {
      margin-left: 20px;
      margin-bottom: 10px;
    }
  }
  .vehicle-types {
    width: 30%;
  }
}
</style>
