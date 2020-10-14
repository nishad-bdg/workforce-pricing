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
      <app-tabs
        :tabs="tabs"
        :currentTabObject.sync="currentTabObject"
      ></app-tabs>
      <!-- tab bar -->
    </div>
    <!-- navbar -->
    <!-- app body -->
    <app-body :currentTabObject.sync="currentTabObject"></app-body>
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
  data() {
    return {
      currentTabObject: {
        id: 1,
        title: "Business Support",
        pills: "business-support",
        breadcrumb:
          "Customer Support / Telesales / Business Development / Administrators /Account Manager",
        description: [
          {
            id: 1,
            title: "Non-native non-voice Agents",
            time: "7.50 / hour",
          },
          {
            id: 2,
            title: "Non-native non-voice Agents",
            time: "7.50 / hour",
          },
          {
            id: 3,
            title: "Non-native non-voice Agents",
            time: "7.50 / hour",
          },
          {
            id: 4,
            title: "Non-native non-voice Agents",
            time: "7.50 / hour",
          },
        ],
      },
      tabs: [
        {
          id: 1,
          title: "Business Support",
          pills: "business-support",
          breadcrumb:
            "Customer Support / Telesales / Business Development / Administrators /Account Manager",
          description: [
            {
              id: 1,
              title: "Non-native non-voice Agents",
              time: "7.50 / hour",
            },
            {
              id: 2,
              title: "Non-native non-voice Agents",
              time: "7.50 / hour",
            },
            {
              id: 3,
              title: "Non-native non-voice Agents",
              time: "7.50 / hour",
            },
            {
              id: 4,
              title: "Non-native non-voice Agents",
              time: "7.50 / hour",
            },
          ],
        },
        {
          id: 2,
          title: "Design",
          pills: "design",
          breadcrumb: "Design",
          description: [
            {
              id: 5,
              title: "Graphic Design",
              time: "15 / hour",
            },
            {
              id: 6,
              title: "Illustration",
              time: "20 / hour",
            },
            {
              id: 7,
              title: "UI/UX Design",
              time: "25 / hour",
            },
            {
              id: 8,
              title: "Motion/ interaction ",
              time: "25 / hour",
            },
          ],
        },
        {
          id: 3,
          title: "Software Development",
          pills: "software-development",
          breadcrumb: "Software Development",
          description: [
            {
              id: 9,
              title: "Non-native non-voice Agents",
              time: "7.50 / hour",
            },
            {
              id: 10,
              title: "Non-native non-voice Agents",
              time: "7.50 / hour",
            },
            {
              id: 11,
              title: "Non-native non-voice Agents",
              time: "7.50 / hour",
            },
            {
              id: 12,
              title: "Non-native non-voice Agents",
              time: "7.50 / hour",
            },
          ],
        },
      ],
    };
  },
  mounted() {},
  methods: {},
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