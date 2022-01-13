<template>
  <div class="product">
    <div class="wrapper">
      <img :src="Product.img" alt="Image">
      <h3>{{ titleProduct }}</h3>
      <p>{{ Product.category }}</p>
    </div>
  </div>
</template>

<script>
  export default {
    props: {
      Product: {
        type: Object,
      },
    },
    computed: {
      titleProduct() {
        if(this.Product.title.length>=30) {
          return this.Product.title.slice(0,30)+"..."
        }
        else {
          return this.Product.title
        }
      }
    }
  }
</script>

<style  scoped>
.product {
  padding: 10px;
}
.wrapper {
  padding: 15px;
  background-color: #fff;
  text-align: left;
}
.product img {
  width: 100%;
  height: auto;
}
.product h3 {
  font-size: 16px;
  font-weight: 400;
  color: #000;
}
.product p {
    font-size: .8125rem;
    color: #6c757d;
}
</style>