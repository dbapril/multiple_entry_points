<template>
  <div>
    <div class="links-row">
      <div class="table-nav">
        <a
          href
          @click.prevent="showTab = 'all'"
          class="table-nav-link"
          :class="showTab === 'all' ? 'active' : ''"
          >Все</a
        >
        <a
          href
          @click.prevent="showTab = 'tab1'"
          class="table-nav-link"
          :class="showTab === 'tab1' ? 'active' : ''"
          >TAB 1</a
        >
        <a
          href
          @click.prevent="showTab = 'tab2'"
          class="table-nav-link"
          :class="showTab === 'tab2' ? 'active' : ''"
          >TAB 2</a
        >
        <a
          href
          @click.prevent="showTab = 'tab3'"
          class="table-nav-link"
          :class="showTab === 'tab3' ? 'active' : ''"
          >TAB 3</a
        >
      </div>
    </div>
    <div class="tabs-container">
      <template v-if="showTab === 'all'">
        <div class="files-row">
          <div class="file-info">
            <p class="file-name">Lorem ipsum Lorem ipsum</p>
            <span>0.42 мб</span>
            <span class="delimiter">|</span>
            <span>28.05.2019 15:53</span>
          </div>
          <a href class="download-link" @click.prevent>
            <img src="../assets/images/download-icon.png" alt />
          </a>
        </div>
        <div class="files-row">
          <div class="file-info">
            <p class="file-name">Lorem ipsum Lorem ipsum</p>
            <span>0.42 мб</span>
            <span class="delimiter">|</span>
            <span>28.05.2019 15:53</span>
          </div>
          <a href class="download-link" @click.prevent>
            <img src="../assets/images/download-icon.png" alt />
          </a>
        </div>
        <div class="files-row">
          <div class="file-info">
            <p class="file-name">Lorem ipsum Lorem ipsum</p>
            <span>0.42 мб</span>
            <span class="delimiter">|</span>
            <span>28.05.2019 15:53</span>
          </div>
          <a href class="download-link" @click.prevent>
            <img src="../assets/images/download-icon.png" alt />
          </a>
        </div>
      </template>
      <template v-if="showTab === 'tab1'">
        <h1>Содержимое вкладки TAB 1</h1>
      </template>
      <template v-if="showTab === 'tab2'">
        <h1>Содержимое вкладки TAB 2</h1>
      </template>
      <template v-if="showTab === 'tab3'">
        <h1>Содержимое вкладки TAB 3</h1>
      </template>
    </div>
  </div>
</template>

<script>
export default {
  name: "FilesTable",
  data: function() {
    return {
      showTab: "all"
    };
  }
};
</script>
