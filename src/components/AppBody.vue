<template>
  <div class="container body-container p-4">
    <div class="d-flex flex-column">
      <!-- card -->
      <div class="card" style="width: 18rem">
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
  max-width: 700px;
  .card {
    width: 550px !important;
    height: 62px !important;
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