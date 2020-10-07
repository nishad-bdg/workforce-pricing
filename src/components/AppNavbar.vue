<template>
  <!-- navbar -->
  <div class="custom-navbar-light align-items-start p-4">
    <div class="d-flex flex-row justify-content-between">
      <div class="">
        <a class="navbar-brand" href="#">
          <img src="../assets/images/logo.svg" alt="logo" />
        </a>
      </div>
      <div class="" align="right">
        <a href="#" class="profile-pic">
          <div>
            <img
              class="profile-pic-circle"
              src="../assets/images/photo.svg"
              alt=""
            />
            <span class="badge badge-pill">
              <img src="../assets/images/online.svg" alt="" />
            </span>
          </div>
        </a>
      </div>
    </div>

    <!-- tab bar -->
    <div class="container-fluid tab-container">
      <div class="d-flex flex-row align-items-center">
        <app-tabs></app-tabs>
      </div>
    </div>
    <!-- tab bar -->
  </div>
  <!-- navbar -->
</template>

<script>
import AppTabs from "@/components/AppTabs";
export default {
  name: "AppNavbar",
  components: {
    "app-tabs": AppTabs,
  },
};
</script>

<style lang="scss" scoped>
.custom-navbar-light {
  max-width: 1920px;
  widows: 1920px;
  height: 250px !important;
  background: #ffffff !important;
  box-shadow: 0px 0px 100px rgba(0, 0, 0, 0.05);
}

.profile-pic-circle {
  width: 50px;
  height: 50px;
  border-radius: 100%;
}
.badge-pill {
  padding-left: 0px;
  padding-right: 0px;
  img {
    margin-top: -42px;
    margin-left: -22px;
  }
}
.tab-container{
  padding-top: 30px;
  padding-left: 200px;
  padding-right: 200px;
}
</style>