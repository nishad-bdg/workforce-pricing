<template>
  <div class="container tab-container">
    <div class="d-flex flex-row justify-content-between">
      <div class="tab-header">Remote Talent - Price List</div>
      <!-- Dropdown -->
      <div class="dropdown">
        <button
          class="btn dropdown-toggle-custom"
          type="button"
          @click="currencyMenu = !currencyMenu"
        >
          <div class="d-flex flex-row justify-content-between">
            <div>{{ selectedCurrency.title }}</div>
            <img src="../assets/images/dropdown-arrow.svg" alt="" />
          </div>
        </button>
        <div
          class="custom-dropdown-menu-item"
          v-show="currencyMenu"
          aria-labelledby="dropdownMenu2"
        >
          <button
            class="dropdown-item btn btn-link"
            type="button"
            v-for="item in currencies"
            :key="item.id"
            @click="selectCurrency(item)"
          >
            {{ item.title }}
          </button>
        </div>
      </div>
      <!-- Dropdown -->
    </div>

    <!-- tabs -->
    <div class="d-flex flex-row justify-content-between tab-bar">
      <nav class="nav">
        <a
          class="nav-link custom-tab mr-4"
          href="#"
          @click="tabClick(tab)"
          v-for="tab in tabs"
          :key="tab.id"
          :class="[tab.id == currentTabObject.id ? 'active' : '']"
          >{{ tab.title }}

          <div
            :class="currentTabObject.id == 2 ? 'slider-shrink' : 'slider'"
            v-show="tab.id == currentTabObject.id"
          ></div>
        </a>
      </nav>
    </div>

    <!-- tabs -->
  </div>
</template>
<script>
export default {
  name: "AppTabs",
  components: {},
  props: {
    tabs: {
      type: Array,
    },
    currentTabObject: {
      type: Object,
    },
  },
  data() {
    return {
      currencyMenu: false,
      selectedCurrency: { id: 1, title: "USD" },
      currencies: [
        { id: 1, title: "USD" },
        { id: 2, title: "GBP" },
        { id: 3, title: "AUD" },
        { id: 4, title: "CAD" },
        { id: 5, title: "EUR" },
        { id: 6, title: "NZD" },
      ],
    };
  },
  methods: {
    tabClick(tab) {
      this.$emit("update:currentTabObject", {
        id: tab.id,
        title: tab.title,
        breadcrumb: tab.breadcrumb,
        description: tab.description,
      });
    },
    selectCurrency(item) {
      this.selectedCurrency = item;
      this.currencyMenu = false;
    },
  },
};
</script>

<style scoped lang="scss">
$primary-color: #0046fe;
.tab-container {
  max-width: 650px;
  margin-left: 16rem;
  @media screen and (max-width: 1263px) {
    margin-left: auto;
  }
}
.tab-bar {
  margin-top: 57px;
}
.tab-header {
  font-family: "Noto Sans";
  font-style: normal;
  font-weight: 600;
  font-size: 24px;
  line-height: 33px;
  text-align: center;
  color: #405899;
}
.dropdown-toggle-custom {
  width: 96px;
  height: 34px !important;
  background: #ffffff !important;
  box-shadow: 0px 20px 100px rgba(0, 43, 156, 0.15);
  border-radius: 5px;
  border-color: #ffffff;
  font-family: "Noto Sans" !important;
  font-style: normal;
  font-weight: 500;
  font-size: 14px;
  line-height: 19px;
  color: #0046fe;
}
.dropdown-item {
  font-family: "Noto Sans" !important;
  font-style: normal;
  font-weight: 500;
  font-size: 14px;
  line-height: 19px;
  color: #0046fe;
  border: none !important;
}
.custom-dropdown-menu-item {
  position: absolute;
  width: 96px;
  background: #ffffff;
  box-shadow: 0px 20px 100px rgba(0, 43, 156, 0.15);
  border-radius: 0px 0px 5px 5px;
}

.custom-tab {
  font-family: "Noto Sans";
  font-style: normal;
  font-weight: 500;
  font-size: 16px;
  line-height: 22px;
  text-align: center;
  color: #d5d5d6 !important;
}
.active {
  color: $primary-color !important;
}
.slider {
  position: absolute;
  width: 91px;
  height: 4px;
  background: #0046fe;
  margin-top: 8px;
  border-radius: 10px 10px 0px 0px;
}
.slider-shrink {
  position: absolute;
  width: 44px;
  height: 4px;
  background: #0046fe;
  margin-top: 8px;
  border-radius: 10px 10px 0px 0px;
}
.nav-link {
  padding-left: 0;
  padding-right: 20px;
}
</style>