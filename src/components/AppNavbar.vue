<template>
  <div>
    <!-- navbar -->
    <div class="custom-navbar-light align-items-start">
      <div class="d-flex flex-row justify-content-between p-4">
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
      <app-tabs></app-tabs>
      <!-- tab bar -->
    </div>
    <!-- navbar -->
    <!-- app body -->
    <app-body></app-body>
    <!-- app body -->
  </div>
</template>

<script>
import AppTabs from "@/components/AppTabs";
import AppBody from "@/components/AppBody";
export default {
  name: "AppNavbar",
  components: {
    "app-tabs": AppTabs,
    "app-body": AppBody,
  },
};
</script>

<style lang="scss" scoped>
.custom-navbar-light {
  max-width: 1920px;
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

// app body
</style>