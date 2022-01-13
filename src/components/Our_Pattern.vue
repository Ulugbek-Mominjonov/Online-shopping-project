<template>
  <div class="wrapper">
    <div>
      <img class="pattern-img" :src="pattern.img" alt="">
    </div>
  </div>
</template>

<script>
  export default {
    props: {
      pattern: {
        type: Object
      },
    },
  }
</script>

<style scoped>
  .wrapper div {
    width: 172px;
    margin: 0 5px;
    padding: 12px;
    border: 1px solid #e1e1e1;
    background-color: #fff;
  }
  .pattern-img {
      filter: grayscale(100%);
      height: 55px;
  }
  .pattern-img:hover {
      filter: grayscale(0);
  }
</style>