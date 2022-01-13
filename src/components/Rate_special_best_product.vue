<template>
  <div class="d-flex align-items-center wrapper">
    <div class="img-wrapper">
      <img :src="product.img" alt="Image" width="92px" height="92px">
    </div>
    <div class="content">
      <h3 class="content-title">{{ product.title }}</h3>
      <p class="content-category">{{ product.category }}</p>
    </div>
  </div>
</template>

<script>
  export default {
    props: {
      product: {
        type: Object
      },
    },
  }
</script>

<style scoped>
.wrapper {
  padding: 10px;
  padding-bottom: 15px;
  background-color: #fff;
  color: #000;
}
.img-wrapper {
  width: 40%;
}
.img-wrapper img {
  width: 100%;
}
.content {
  text-align: left;
}
.content-title {
  font-size: 15px;
  line-height: 18px;

}
.content-category {
  font-size: 14px;
  color: #c94a00;
}
</style>