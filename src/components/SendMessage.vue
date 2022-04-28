<template>
  <section>
    <div class="container">
      <div class="container-section-message">
        <!-- sezione left  -->
        <div class="send-message">
          <p class="p-intro">SEND A MESSAGE</p>
          <h1>Get in <span class="light">Touch</span></h1>
          <p>We will respond to your message as soon as possible.</p>
          <div class="name-email">
            <input type="text" placeholder="Name" required />
            <input type="email" placeholder="Email" required />
          </div>
          <div class="name-email">
            <input type="number" placeholder="Phone" required />
            <select class="form-select">
              <option selected>More Info</option>
              <option value="1">Cliente</option>
              <option value="2">Nuovo Cliente</option>
              <option value="3">Supporto</option>
            </select>
          </div>
          <textarea
            name="Message"
            id="prova"
            cols="107"
            rows="10"
            placeholder="Messages"
          ></textarea>
          <div class="btn-message">
            <button class="btn-header">SEND</button>
          </div>
        </div>
        <!-- sezione right  -->
        <div class="contacts">
          <h3>Exemple Inc.</h3>
          <p>
            Lorem ipsum dolor sit amet consectetur adipisicing elit. Non,
            expedita dolores.
          </p>
          <p>
            Lorem ipsum dolor sit amet consectetur adipisicing elit. Non,
            expedita dolores.
          </p>
          <div>
            <font-awesome-icon class="icon" icon="fa-solid fa-phone" />
            <span><a href="#">+1(305) 1234-5678</a></span>
          </div>
          <div>
            <font-awesome-icon class="icon" icon="fa-solid fa-envelope" />
            <span><a href="#">hello@example.com</a></span>
          </div>
          <div>
            <font-awesome-icon class="icon" icon="fa-solid fa-envelope" />
            <span><a href="#">Main Avenue, 987</a></span>
          </div>
          <div>
            <button class="btn-trasparent">VIEW MAP</button>
          </div>
        </div>
      </div>
    </div>
  </section>
  <!-- collegare al main il componente  -->
</template>

<script>
export default {
  name: "SendMessage",
};
</script>

<style lang="scss" scoped>
@import "@/assets/style/variabili.scss";

section {
  padding: $padding-section;
  .container-section-message {
    display: flex;
    justify-content: space-between;
    .send-message {
      width: 65%;
      .p-intro {
        padding-bottom: 25px;
      }
      h1 {
        font-size: $font-size-title;
        padding-bottom: 25px;
        & + p {
          color: $color-text-darker;
          padding-bottom: 35px;
        }
      }
      .name-email {
        display: flex;
        justify-content: space-between;
        padding-bottom: 10px;
        & input {
          width: 49%;
          padding: 10px;
          border: none;
          background-color: #ececec;
          border-radius: 5px;
        }
        .form-select {
          width: 49%;
          border: none;
          background-color: #ececec;
          border-radius: 5px;
          padding-left: 5px;
          color: $color-text-darker;
        }
      }
      #prova {
        background-color: #ececec;
        border: none;
        padding: 10px;
        width: 100%;
        border-radius: 5px;
      }
      .btn-message {
        padding-top: 30px;
      }
    }
    .contacts {
      width: 30%;
      & > * {
        padding-bottom: 20px;
      }
      & p {
        color: $color-text-darker;
      }
      .icon,
      a {
        color: $bg-button;
      }
      span {
        margin-left: 15px;
      }
      .icon {
        background-color: #daeced;
        padding: 10px;
        border-radius: 50%;
      }
      div {
        display: flex;
        align-items: center;
      }
      .btn-trasparent {
        background-color: white;
        color: $bg-button;
        &:active {
          background-color: #52bbbb;
        }
      }
    }
  }
}
</style>