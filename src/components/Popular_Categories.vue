<template>
  <div class="wrapper">
    <h2 class="title">
      <router-link to="#" class="link">{{ PopularCat.title}}</router-link>
    </h2>
    <ul class="feature_list">
      <li class="feature_item" v-for="item in Feature" :key="item">
        <router-link class="link" to="#">{{ item }}</router-link>
      </li>
    </ul>
    <router-link class="link popular-link" to="#">View more</router-link>
  </div>
</template>

<script>
  export default {
    props: {
      PopularCat: {
        type: Object
      },
    },
    computed: {
      Feature() {
        return this.PopularCat.feature.slice(0,4)
      }
    }
  }
</script>

<style scoped>
.wrapper {
  padding: 24px;
  background-color: #fff;
  text-align: left;
}
.title {
  font-weight: 500;
  font-size: 18px;
  line-height: 24px;
}
.title .link {
  color: #000;
}
.feature_list {
  margin: 0;
  margin-top: 10px;
  padding-left: 20px;
  list-style-type: square;
}
.feature_item {
    padding-left: 11px;
    padding-right: 0;
    color: #6c757d;
    padding-top: 5px;
    padding-bottom: 5px;
    font-size: 15px;
}
.feature_item .link {
  color: #6c757d;
}
.popular-link {
  display: block;
  margin-top: 10px;
  font-size: 14px;
  font-weight: 500;
  color: #f47a1d;
}
.popular-link:hover {
  color: #c94a00;
}
</style>