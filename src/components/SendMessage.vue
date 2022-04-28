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
            <input v-model="datiNome" type="text" placeholder="Name" required />
            <input
              v-model="datiEmail"
              type="email"
              placeholder="Email"
              required
            />
          </div>
          <div class="name-email">
            <input
              v-model="datiPhone"
              type="text"
              placeholder="Phone"
              required
            />
            <select class="form-select">
              <option selected>More Info</option>
              <option value="1">Cliente</option>
              <option value="2">Nuovo Cliente</option>
              <option value="3">Supporto</option>
            </select>
          </div>
          <textarea
            v-model="datiArea"
            name="Message"
            id="prova"
            cols="107"
            rows="10"
            placeholder="Messages"
          ></textarea>
          <div class="btn-message">
            <button @click="datiInseriti" class="btn-header">SEND</button>
            <span v-if="this.showMessage === 2"
              ><font-awesome-icon
                class="icon"
                icon="fa-solid fa-circle-check"
              />Messaggio inoltrato con successo! Un nostro operatore ti
              contatterà a breve</span
            >
            <span class="error-message" v-if="this.showMessage === 3"
              ><font-awesome-icon
                class="icon"
                icon="fa-solid fa-circle-xmark"
              />Messaggio non inoltrato! Inserisci tutti i campi</span
            >
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
            <font-awesome-icon
              class="icon dot"
              icon="fa-solid fa-location-dot"
            />
            <span><a href="#">Main Avenue, 987</a></span>
          </div>
          <div>
            <button @click="goToGoogleMaps" class="btn-trasparent">
              VIEW MAP
            </button>
          </div>
          <div v-if="showMaps === true" class="img-maps">
            <img
              src="https://i.stack.imgur.com/uzHgF.png"
              alt="Main Avenue,97"
            />
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
  data() {
    return {
      showMaps: false,
      datiNome: "",
      datiEmail: "",
      datiPhone: "",
      datiArea: "",
      showMessage: 1,
    };
  },
  methods: {
    goToGoogleMaps() {
      this.showMaps = !this.showMaps;
    },
    datiInseriti() {
      if (
        this.datiNome.length > 0 &&
        this.datiEmail.length > 0 &&
        this.datiPhone.length > 0 &&
        this.datiArea.length > 0
      ) {
        this.showMessage = 2;
        this.datiNome = "";
        this.datiEmail = "";
        this.datiPhone = "";
        this.datiArea = "";
      } else {
        this.showMessage = 3;
        this.datiNome = "";
        this.datiEmail = "";
        this.datiPhone = "";
        this.datiArea = "";
      }
    },
  },
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
        padding-top: 40px;
        span {
          margin-left: 15px;
          padding: 10px;
          color: $bg-button;
        }
        .error-message {
          margin-left: 15px;
          padding: 10px;
          color: red;
        }
        .icon {
          margin-right: 5px;
        }
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
        &.dot {
          padding: 10px 13px;
        }
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
      .img-maps {
        width: 180px;
        padding-bottom: 0px;
        img {
          width: 100%;
        }
      }
    }
  }
}
</style>