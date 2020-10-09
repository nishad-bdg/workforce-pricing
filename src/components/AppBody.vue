<template>
  <div class="container body-container">
    <div class="d-flex flex-column">
      <div class="breadcrumb-text mt-sm-5 mt-4 mb-4">
        {{ currentTabObject.breadcrumb }}
      </div>

      <div class="progress mb-4 d-sm-flex d-none">
        <div
          class="progress-bar"
          role="progressbar"
          style="width: 30%"
          aria-valuenow="25"
          aria-valuemin="0"
          aria-valuemax="100"
        ></div>
      </div>
      <!-- card -->
      <div
        class="card mb-4"
        v-for="item in currentTabObject.description"
        :key="item.id"
      >
        <div class="card-body">
          <div class="d-flex flex-row justify-content-between">
            <div class="custom-card-title">
              {{ item.title }} <span class="ml-3">- {{ item.time }}</span>
            </div>
            <div class="custom-card-title d-sm-flex d-none">
              Choose candidates
            </div>
            <div class="mobile-eye d-sm-none d-flex">
              <img src="../assets/images/eye.svg" alt="" />
            </div>
          </div>
        </div>
      </div>
      <!-- card -->
    </div>
  </div>
</template>
<script>
export default {
  name: "AppBody",
  props: {
    currentTabObject: {
      type: Object,
    },
  },
};
</script>
<style lang="scss" scoped>
.body-container {
  max-width: 650px;
  margin-left: 16rem;
  @media screen and (max-width: 1263px) {
    margin-left: auto;
  }
  .breadcrumb-text {
    font-family: "Noto Sans";
    font-style: normal;
    font-weight: 500;
    font-size: 14px;
    line-height: 19px;
    color: #d5d5d6;
    @media screen and (max-width: 424px){
      font-size: 12px;
    }
    @media screen and (max-width: 340px){
      font-size: 10px;
    }
  }

  .progress {
    width: 550px;
    height: 3px;
    background: #edf2ff;
    .progress-bar {
      background: #0046fe;
    }
  }
  .card {
    width: 550px !important;
    height: 62px !important;
    background: #ffffff;
    box-shadow: 0px 20px 100px rgba(0, 43, 156, 0.15);
    border-color: transparent;
    border-radius: 5px;
    @media screen and (max-width: 599px) {
      width: auto !important;
    }

    @media screen and (max-width: 360px) {
      padding: 0;
    }

    img {
      @media screen and (max-width: 370px) {
        width: 80% !important;
        height: auto;
      }
      @media screen and (max-width: 350px) {
        width: 60% !important;
        height: auto;
      }
    }
    .custom-card-title {
      font-family: "Noto Sans";
      font-style: normal;
      font-weight: 600;
      font-size: 16px;
      line-height: 22px;
      color: #0046fe;
      @media screen and (max-width: 599px) {
        font-size: 14px;
        line-height: 19.07px;
        @media screen and (max-width: 424px) {
          font-size: 12px;
        }
        @media screen and (max-width: 370px) {
          font-size: 10px;
        }
        @media screen and (max-width: 350px) {
          font-size: 8px;
        }
      }
      span {
        font-family: "Noto Sans";
        font-style: normal;
        font-weight: normal;
        font-size: 14px;
        line-height: 19px;
        color: #002178;
        @media screen and (max-width: 424px) {
          font-size: 12px;
        }
        @media screen and (max-width: 370px) {
          font-size: 10px;
        }
        @media screen and (max-width: 350px) {
          font-size: 8px;
        }
      }
    }
  }
}
</style>