<template>
  <div class="container-fluid">
    <div class="d-flex flex-row justify-content-between">
      <div class="tab-header">Remote Talent - Price List</div>
      <div class="">
        <select class="currency-dropdown form-control">
          <option value="usd">USD</option>
          <option value="euro">EURO</option>
        </select>
      </div>
    </div>

    <!-- tabs -->
    <div class="d-flex flex-row justify-content-between mt-5">
      <nav class="nav">
        <a
          class="nav-link custom-tab"
          href="#"
          @click="currentTab = tab.id"
          v-for="tab in tabs"
          :key="tab.id"
          :class="[tab.id == currentTab ? 'active' : '']"
          >{{ tab.title }}
            
          </a
        >
      </nav>
      
    </div>
   <div class="slider"></div>
    <!-- tabs -->
  </div>
</template>
<script>
export default {
  name: "AppTabs",
  components: {
  },
  data() {
    return {
      currentTab: 1,
      tabs: [
        { id: 1, title: "Business Support", pills: "business-support" },
        { id: 2, title: "Design", pills: "design" },
        { id: 3, title: "Software Development", pills: "software-development" },
      ],
    };
  },
};
</script>

<style scoped lang="scss">
$primary-color: #0046fe;
.tab-header {
  font-family: "Noto Sans";
  font-style: normal;
  font-weight: 600;
  font-size: 24px;
  line-height: 33px;
  text-align: center;
  color: #405899;
}
.currency-dropdown {
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
.nav-link{
  padding-left: 0;
  padding-right: 20px;
}
</style>