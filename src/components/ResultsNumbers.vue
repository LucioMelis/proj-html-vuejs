<template>
  <section>
    <div class="container">
      <div>
        <p class="p-intro">WHAT ARE WE DOING</p>
        <h1><span class="dark">Results</span> in Numbers</h1>
      </div>
      <div class="numbers">
        <div>
          <p class="p-intro">128</p>
          <h3>Certifications</h3>
        </div>
        <div>
          <p class="p-intro">230</p>
          <h3>Employees</h3>
        </div>
        <div>
          <p class="p-intro">517</p>
          <h3>Customers</h3>
        </div>
        <div>
          <p class="p-intro">94</p>
          <h3>Countries Served</h3>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
export default {};
</script>

<style lang="scss" scoped>
@import "@/assets/style/variabili.scss";
section {
  background-image: url("@/assets/img/bg-10.jpg");
  background-size: cover;
  background-position: center;
  padding: 100px 0;
  .container > div:first-child {
    text-align: center;
  }
  .numbers {
    display: flex;
    justify-content: space-around;
    text-align: center;
    padding: 60px 0;
    p {
      font-size: 30px;
      font-weight: $font-strong;
    }
  }
}
h1 {
  font-size: $font-size-title;
  color: white;
  padding: 30px 0;
}
h3 {
  color: white;
  font-weight: 600;
}
</style>