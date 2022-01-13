<template>
  <div class="img-wrapper">
    <img class="image" :src="Categories.img" alt="category image" width="35" height="35">
    <h2 class="title">{{Categories.name}}</h2>
  </div>
</template>

<script>
  export default {
    props: {
      Categories: {
        type: Object
      },
      picture: String
    },
  }
</script>

<style scoped>
  .img-wrapper {
    padding: 10px 15px;
  }
  .title {
    font-size: 11px;
    font-weight: 500;
    text-transform: uppercase;
    color: #b3b3b3;
    margin-top: 4px;
    margin-bottom: 0;
    transition: color .15s;
    line-height: 15px;
  }
  .image {
    filter: grayscale(1);
    opacity: .7;
    transition: filter .15s,opacity .15s;
  }
  .img-wrapper:hover .image {
    filter: grayscale(0);
    opacity: 1;
  }
</style>