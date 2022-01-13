<template>
  <div class="news">
    <div class="d-flex news-wrapper">
      <div class="img-warpper">
        <img class="news-img" :src="NewsItem.img" alt="image">
      </div>
      <div class="news-content">
        <h3 class="news-title">{{ NewsItem.title }}</h3>
        <p class="news-text">{{ NewsItem.text }}</p>
        <span class="news-link">Read more</span>        
        <p class="news-data">{{ NewsItem.data }}</p>
      </div>
    </div>
  </div>
</template>

<script>
  export default {
    props: {
      NewsItem: {
        type: Object
      },
    },
  }
</script>

<style scoped>
.news-wrapper {
  color: #000;
  padding-left: 25px;
}
.news-img {
  display: block;
  width: 100%;
  height: 100%;
  object-fit: fill;
}
.news-content {
  padding: 20px;
  background-color: #fff;
  text-align: left;
}
.news-title {
  font-size: 16px;
  line-height: 22px;
  overflow: hidden;
  max-height: 44px;
  text-align: left;
  font-weight: 500;
  margin-bottom: 10px;
  
}
.news-text {
  margin-bottom: 8px;
  font-size: 15px;
  line-height: 22px;
  color: rgba(0,0,0,.83);
}
.news-link {
  font-size: 14px;
  color: #c94a00;
}
.news-data {
  color: #999;
  line-height: 19px;
  font-size: 14px;
  margin-bottom: 0;
}
</style>