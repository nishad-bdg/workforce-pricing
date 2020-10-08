<template>
  <div class="container tab-container">
    <div class="d-flex flex-row justify-content-between">
      <div class="tab-header">Remote Talent - Price List</div>
      <div class="currency-dropdown">
        <select class="form-control">
          <option value="usd">USD</option>
          <option value="euro">EURO</option>
        </select>
      </div>
    </div>

    <!-- tabs -->
    <div class="d-flex flex-row justify-content-between mt-4">
      <nav class="nav">
        <a
          class="nav-link custom-tab"
          href="#"
          @click="tabClick(tab)"
          v-for="tab in tabs"
          :key="tab.id"
          :class="[tab.id == currentTabObject.id ? 'active' : '']"
          >{{ tab.title }}
        </a>
      </nav>
      <br>
    </div>
    <div class="slider"></div>
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
    return {};
  },
  methods: {
    tabClick(tab) {
      this.$emit("update:currentTabObject", {
        id: tab.id,
        title: tab.title,
        breadcrumb: tab.breadcrumb,
        description: tab.description
      });
    },
  },
};
</script>

<style scoped lang="scss">
$primary-color: #0046fe;
.tab-container {
  max-width: 650px;
  padding-top: 52px;
  margin-left: 16rem;
  @media screen and (max-width: 1263px) {
    margin-left: auto;
  }
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
.currency-dropdown select {
  width: 96px;
  height: 34px !important;
  box-shadow: 0px 20px 100px rgba(0, 43, 156, 0.15);
  border-radius: 5px;
  border-color: #ffffff;
  -moz-appearance: none; /* Firefox */
  -webkit-appearance: none; /* Safari and Chrome */
  appearance: none;
  background: transparent;
  background-image: url("../assets/images/dropdown-arrow.svg");
  background-repeat: no-repeat;
  background-position-x: 90%;
  background-position-y: 13px;
  font-family: "Noto Sans";
  font-style: normal;
  font-weight: 500;
  font-size: 14px;
  line-height: 19px;
  color: #0046fe;
  overflow: hidden;
}
.current-dropdown::-ms-expand {
  display: none; /* Remove default arrow in Internet Explorer 10 and 11 */
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
  border-radius: 10px 10px 0px 0px;
}
.nav-link {
  padding-left: 0;
  padding-right: 20px;
}
</style>