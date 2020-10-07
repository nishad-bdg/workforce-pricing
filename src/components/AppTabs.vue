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
  </div>
</template>
<script>
export default {
  name: "AppTabs",
};
</script>

<style scoped lang="scss">
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
  background-position-x: 100%;
  background-position-y: 13px;
}
</style>