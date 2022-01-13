<template>
  <div class="sms">
    Post RFG
  </div>
</template>

<script>
  export default {
    
  }
</script>

<style scoped>
  .sms {
    display: flex;
    align-items: center;
    font-size: 14px;
    font-weight: 500;
    color: #262626;
  }
  .sms::before {
    display: block;
    content: "";
    width: 22px;
    height: 22px;
    margin-right: 5px;
    background-image: url("../assets/img/sms.webp");
    background-size: contain;
  }
</style>