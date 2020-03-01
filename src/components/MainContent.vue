<template>
  <main class="main-content">
    <div class="interior-wrapper">
      <section class="short-info">
        <h1>Lorem ipsum dolor, consectetur adipiscing elit</h1>
        <p>
          Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do
          eiusmod
        </p>
        <p>
          Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do
          eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad
          minim veniam, quis nostrud exercitation ullamco laboris nisi ut
          aliquip ex ea commodo consequat. Duis aute irure dolor in
          reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla
          pariatur.
        </p>
      </section>
      <section class="cards-section">
        <h2>Lorem ipsum dolor sit</h2>
        <div class="gallery">
          <div
            class="card-block"
            v-for="card in cards"
            :key="card"
            :id="'card_' + card"
            @mouseenter="toggleCardText($event)"
            @mouseleave="toggleCardText($event)"
          >
            <p class="card-header">Lorem ipsum dolor sit amet</p>
            <p class="card-text" hidden>
              Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do
              eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut
              enim ad minim veniam, quis nostrud exercitation ullamco laboris
            </p>
          </div>
        </div>
      </section>
      <section class="location-section">
        <h2 id="locationHeader">МЕСТОПОЛОЖЕНИЕ</h2>
        <p>
          Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do
          eiusmod Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed
          do eiusmod
        </p>
        <p>
          Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do
          eiusmod Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed
          do eiusmod
        </p>
        <div class="ya-map-block" id="map"></div>
      </section>
      <section class="files-section">
        <h2 id="filesHeader">ФАЙЛЫ</h2>
        <FilesTable />
      </section>
    </div>
  </main>
</template>

<script>
import FilesTable from "./FilesTable.vue";

export default {
  name: "MainContent",
  components: {
    FilesTable
  },
  data: function() {
    return {
      cards: [1, 2, 3, 4, 5, 6, 7, 8, 9]
    };
  },
  methods: {
    toggleCardText: function(event) {
      document
        .querySelector(`#${event.target.id}`)
        .querySelector(".card-text")
        .toggleAttribute("hidden");
    }
  }
};
</script>
