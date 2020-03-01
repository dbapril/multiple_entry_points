<template>
  <main class="main-content form-main-content">
    <div class="interior-wrapper">
      <h1 class="form-header">
        Lorem ipsum
        <br />dolor
      </h1>
      <form class="main-form" action="/">
        <input
          type="tel"
          class="tel-input"
          id="phone"
          placeholder="Ваш телефон*"
          required
        />
        <button type="submit" class="submit-button">ОТПРАВИТЬ</button>
        <div class="accept">
          <input
            class="styled-checkbox"
            id="styled-checkbox-1"
            type="checkbox"
            value="value1"
            checked
            required
          />
          <label for="styled-checkbox-1">Я принимаю условия</label>
        </div>
      </form>
    </div>
  </main>
</template>

<script>
import Inputmask from "inputmask";

export default {
  name: "FormMainContent",
  methods: {
    toggleCardText: function(event) {
      document
        .querySelector(`#${event.target.id}`)
        .querySelector(".card-text")
        .toggleAttribute("hidden");
    }
  },
  mounted() {
    let m = new Inputmask("999-999-99-99");
    m.mask(document.querySelector("#phone"));
  }
};
</script>
