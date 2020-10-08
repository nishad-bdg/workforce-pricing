<template>
  <div class="container body-container">
    <div class="d-flex flex-column">
      <div class="custom-support-text mt-5 mb-4">
        Customer Support / Telesales / Business Development / Administrators /
        Account Manager
      </div>

      <div class="progress mb-4">
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
      <div class="card mb-4" v-for="i in 4" :key="i">
        <div class="card-body">
          <div class="d-flex flex-row justify-content-between">
            <div class="custom-card-title">Non-native non-voice Agents</div>
            <div class="time">- 7.50 / hour</div>
            <div class="custom-card-title">Choose candidates</div>
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
  
};
</script>
<style lang="scss" scoped>
.body-container {
  max-width: 650px;
  margin-left: 16rem;
  @media screen and (max-width: 1263px){
    margin-left: auto;
  }
  .custom-support-text {
    font-family: "Noto Sans";
    font-style: normal;
    font-weight: 500;
    font-size: 14px;
    line-height: 19px;
    color: #d5d5d6;
  }

  .progress {
    width: 550px;
    height: 3px;
    background: #EDF2FF;
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
    .custom-card-title {
      font-family: "Noto Sans";
      font-style: normal;
      font-weight: 600;
      font-size: 16px;
      line-height: 22px;
      color: #0046fe;
    }
    .time {
      font-family: "Noto Sans";
      font-style: normal;
      font-weight: normal;
      font-size: 14px;
      line-height: 19px;
      color: #002178;
    }
  }
}
</style>