<template>
  <div class="home container">
    <!-- Categories -->
    <div class="row categories-wrapper">
      <div class="col category-col" v-for="item in categories" :key="item">
        <Category class="category"  :Categories="item" :picture="item.img" />
      </div>
    </div>

    <!-- Popular categories -->
    <div class="row popular-category">
      <div class="col-12">
        <h2 class="title">Popular Categories</h2>
      </div>
      <div class="col-4 category_item" v-for="item in feature_cetegories" :key="item">
        <PopularCategories :PopularCat="item" />
      </div>
    </div>

    <!-- Product -->
    <div class="row product-row">
        <div class="col product-col">
          <h2 class="product-title">Feature Product</h2>
          <router-link class="link" to="#">
            <VueSlickCarousel v-bind="settings">
             <ProductFeature v-for="item in feature_Products" :key="item" :Product="item" />
            </VueSlickCarousel>
          </router-link>
        </div>
    </div>

    <!-- Form  -->
    <div class="row form-row">
      <div class="col-5 form-left">
        <div>
          <h2 class="form-left_title">LET THE SUPPLIER FIND YOU WITH RFQ</h2>
          <p class="form-left_text">Fast Response from premium suppliers One request, Multiple Quotes Reach Global Suppliers Accurate Business Matchmaking</p>
        </div>
      </div>
      <div class="col-7 form-right">
        <span>Get Free Quotes From Multiple Sellers</span>
        <form class="form_form">
          <div class="d-flex justify-content-between form_form_input">
            <input class="form-control" type="text" placeholder="Product name" name="product_name">
            <input class="form-control" type="text" placeholder="Quantity" name="quantity">
            <input class="form-control" type="number" placeholder="Expected Price" name="price">
          </div>
          <div class="form-floating">
            <textarea class="form-control" placeholder="Leave a comment here" id="floatingTextarea" rows="5"></textarea>
            <label for="floatingTextarea">Comments</label>
          </div>
          <div class="button">
            <button type="button">Request For Quantation</button>
          </div>
        </form>
      </div>
    </div>

    <!-- Pattern  -->
    <div class="row our-pattern">
      <div class="col pattern-col">
        <h2 class="product-title pattern-title">Our Patterns</h2>
        <router-link class="link" to="#">
            <VueSlickCarousel v-bind="settings2">
              <OurPattern v-for="item in patterns" :key="item" :pattern="item" />
            </VueSlickCarousel>
        </router-link>
      </div>
    </div>

    <!-- News  -->
    <div class="row news-row">
      <div class="col">
        <h2 class="product-title news-title">Latest News</h2>
        <router-link class="link" to="#">
            <VueSlickCarousel v-bind="settings3">
              <News v-for="item in news" :key="item" :NewsItem="item" />
            </VueSlickCarousel>
        </router-link>
      </div>
    </div>

    <!-- Rate Special Bestseller Product  -->
    <div class="row rate-special-best">
      <div class="col-4 rated-product">
          <h2 class="product-title rate-title">Top Rated Products</h2>
          <ul class="product-list list-unstyled">
            <li class="product-item"  v-for="item in rate" :key="item">
              <router-link class="link" to="#">
                <RateSpecialBest :product="item" />
              </router-link>
            </li>
          </ul>
      </div>

      <div class="col-4 rated-product">
          <h2 class="product-title rate-title">Special Offers</h2>
          <ul class="product-list list-unstyled">
            <li class="product-item"  v-for="item in rate" :key="item">
              <router-link class="link" to="#">
                <RateSpecialBest :product="item" />
              </router-link>
            </li>
          </ul>
      </div>

      <div class="col-4 rated-product">
          <h2 class="product-title rate-title">Bestsellers</h2>
          <ul class="product-list list-unstyled">
            <li class="product-item"  v-for="item in rate" :key="item">
              <router-link class="link" to="#">
                <RateSpecialBest :product="item" />
              </router-link>
            </li>
          </ul>
      </div>
    </div>
  </div>
</template>

<script>
// Import Components 
import Category from '@/components/Category.vue';
import PopularCategories from '@/components/Popular_Categories.vue';
import ProductFeature from '@/components/ProductFeature.vue';
import OurPattern from '@/components/Our_Pattern.vue';
import News from '@/components/News.vue';
import RateSpecialBest from '@/components/Rate_special_best_product.vue';

// Slick Carousel 
import VueSlickCarousel from 'vue-slick-carousel'
import 'vue-slick-carousel/dist/vue-slick-carousel.css'
import 'vue-slick-carousel/dist/vue-slick-carousel-theme.css'

  export default {
    components: {
      Category,
      PopularCategories,
      VueSlickCarousel,
      ProductFeature,
      OurPattern,
      News,
      RateSpecialBest
    },
    data() {
      return {
        categories: [
          {
            img: "https://alietc.com/themes/velocity/assets/images/brand-1.webp",
            name: "Apparel",
          },
          {
            img: "https://alietc.com/themes/velocity/assets/images/brand-1.webp",
            name: "Apparel",
          },
          {
            img: "https://alietc.com/themes/velocity/assets/images/brand-1.webp",
            name: "Apparel",
          },
          {
            img: "https://alietc.com/themes/velocity/assets/images/brand-1.webp",
            name: "Apparel",
          },
          {
            img: "https://alietc.com/themes/velocity/assets/images/brand-1.webp",
            name: "Apparel",
          },
          {
            img: "https://alietc.com/themes/velocity/assets/images/brand-1.webp",
            name: "Apparel",
          },
          {
            img: "https://alietc.com/themes/velocity/assets/images/brand-1.webp",
            name: "Apparel",
          },
          {
            img: "https://alietc.com/themes/velocity/assets/images/brand-1.webp",
            name: "Apparel",
          },
          {
            img: "https://alietc.com/themes/velocity/assets/images/brand-1.webp",
            name: "Apparel",
          },
          {
            img: "https://alietc.com/themes/velocity/assets/images/brand-1.webp",
            name: "Apparel",
          },
          {
            img: "https://alietc.com/themes/velocity/assets/images/brand-1.webp",
            name: "Apparel",
          },
          {
            img: "https://alietc.com/themes/velocity/assets/images/brand-1.webp",
            name: "Apparel",
          },
          {
            img: "https://alietc.com/themes/velocity/assets/images/brand-1.webp",
            name: "Apparel",
          },
          {
            img: "https://alietc.com/themes/velocity/assets/images/brand-1.webp",
            name: "Apparel",
          },
          {
            img: "https://alietc.com/themes/velocity/assets/images/brand-1.webp",
            name: "Apparel",
          },
          {
            img: "https://alietc.com/themes/velocity/assets/images/brand-1.webp",
            name: "Apparel",
          },
          {
            img: "https://alietc.com/themes/velocity/assets/images/brand-1.webp",
            name: "Apparel",
          },
          {
            img: "https://alietc.com/themes/velocity/assets/images/brand-1.webp",
            name: "Apparel",
          },
          {
            img: "https://alietc.com/themes/velocity/assets/images/brand-1.webp",
            name: "Apparel",
          },
          {
            img: "https://alietc.com/themes/velocity/assets/images/brand-1.webp",
            name: "Apparel",
          },
          {
            img: "https://alietc.com/themes/velocity/assets/images/brand-1.webp",
            name: "Apparel",
          },
          {
            img: "https://alietc.com/themes/velocity/assets/images/brand-1.webp",
            name: "Apparel",
          },
          {
            img: "https://alietc.com/themes/velocity/assets/images/brand-1.webp",
            name: "Apparel",
          },
          {
            img: "https://alietc.com/themes/velocity/assets/images/brand-1.webp",
            name: "Apparel",
          },
          {
            img: "https://alietc.com/themes/velocity/assets/images/brand-1.webp",
            name: "Apparel",
          },
          {
            img: "https://alietc.com/themes/velocity/assets/images/brand-1.webp",
            name: "Apparel",
          },
          {
            img: "https://alietc.com/themes/velocity/assets/images/brand-1.webp",
            name: "Apparel",
          },
          {
            img: "https://alietc.com/themes/velocity/assets/images/brand-1.webp",
            name: "Apparel",
          },
          {
            img: "https://alietc.com/themes/velocity/assets/images/brand-1.webp",
            name: "Apparel",
          },
          {
            img: "https://alietc.com/themes/velocity/assets/images/brand-1.webp",
            name: "Apparel",
          },
          {
            img: "https://alietc.com/themes/velocity/assets/images/brand-1.webp",
            name: "Apparel",
          },
          {
            img: "https://alietc.com/themes/velocity/assets/images/brand-1.webp",
            name: "Apparel",
          },
          {
            img: "https://alietc.com/themes/velocity/assets/images/brand-1.webp",
            name: "Apparel",
          },
          {
            img: "https://alietc.com/themes/velocity/assets/images/brand-1.webp",
            name: "Apparel",
          },
          {
            img: "https://alietc.com/themes/velocity/assets/images/brand-1.webp",
            name: "Apparel",
          },
          {
            img: "https://alietc.com/themes/velocity/assets/images/brand-1.webp",
            name: "Apparel",
          },
          
        ],
        feature_cetegories: [
          {
            title: "Food  & Beverage",
            feature: [
              "Baby Food", "Bean Products", "Baked Goods", "Alcoholic Beverage"
            ]
          },
          {
            title: "Food  & Beverage",
            feature: [
              "Baby Food", "Bean Products", "Baked Goods", "Alcoholic Beverage"
            ]
          },
          {
            title: "Food  & Beverage",
            feature: [
              "Baby Food", "Bean Products", "Baked Goods", "Alcoholic Beverage"
            ]
          },
          {
            title: "Food  & Beverage",
            feature: [
              "Baby Food", "Bean Products", "Baked Goods", "Alcoholic Beverage"
            ]
          },
          {
            title: "Food  & Beverage",
            feature: [
              "Baby Food", "Bean Products", "Baked Goods", "Alcoholic Beverage"
            ]
          },
          {
            title: "Food  & Beverage",
            feature: [
              "Baby Food", "Bean Products", "Baked Goods", "Alcoholic Beverage"
            ]
          },
          {
            title: "Food  & Beverage",
            feature: [
              "Baby Food", "Bean Products", "Baked Goods", "Alcoholic Beverage"
            ]
          },
          {
            title: "Food  & Beverage",
            feature: [
              "Baby Food", "Bean Products", "Baked Goods", "Alcoholic Beverage"
            ]
          },
          {
            title: "Food  & Beverage",
            feature: [
              "Baby Food", "Bean Products", "Baked Goods", "Alcoholic Beverage"
            ]
          },          
        ],
        feature_Products: [
          {
            title: "Top Quality South African Strelitzia Nicolai Seeds",
            img: "https://alietc.com/cache/medium/product/8910/u8aACJjpwk5wvQrlkqMg.webp",
            category: "Food  & Beverage"
          },
          {
            title: "Top Quality South African Strelitzia Nicolai Seeds",
            img: "https://alietc.com/cache/medium/product/8910/u8aACJjpwk5wvQrlkqMg.webp",
            category: "Food  & Beverage"
          },
          {
            title: "Top Quality South African Strelitzia Nicolai Seeds",
            img: "https://alietc.com/cache/medium/product/8910/u8aACJjpwk5wvQrlkqMg.webp",
            category: "Food  & Beverage"
          },
          {
            title: "Top Quality South African Strelitzia Nicolai Seeds",
            img: "https://alietc.com/cache/medium/product/8910/u8aACJjpwk5wvQrlkqMg.webp",
            category: "Food  & Beverage"
          },
          {
            title: "Top Quality South African Strelitzia Nicolai Seeds",
            img: "https://alietc.com/cache/medium/product/8910/u8aACJjpwk5wvQrlkqMg.webp",
            category: "Food  & Beverage"
          },
          {
            title: "Top Quality South African Strelitzia Nicolai Seeds",
            img: "https://alietc.com/cache/medium/product/8910/u8aACJjpwk5wvQrlkqMg.webp",
            category: "Food  & Beverage"
          },
          {
            title: "Top Quality South African Strelitzia Nicolai Seeds",
            img: "https://alietc.com/cache/medium/product/8910/u8aACJjpwk5wvQrlkqMg.webp",
            category: "Food  & Beverage"
          },
          {
            title: "Top Quality South African Strelitzia Nicolai Seeds",
            img: "https://alietc.com/cache/medium/product/8910/u8aACJjpwk5wvQrlkqMg.webp",
            category: "Food  & Beverage"
          },
          {
            title: "Top Quality South African Strelitzia Nicolai Seeds",
            img: "https://alietc.com/cache/medium/product/8910/u8aACJjpwk5wvQrlkqMg.webp",
            category: "Food  & Beverage"
          },
          {
            title: "Top Quality South African Strelitzia Nicolai Seeds",
            img: "https://alietc.com/cache/medium/product/8910/u8aACJjpwk5wvQrlkqMg.webp",
            category: "Food  & Beverage"
          },
          {
            title: "Top Quality South African Strelitzia Nicolai Seeds",
            img: "https://alietc.com/cache/medium/product/8910/u8aACJjpwk5wvQrlkqMg.webp",
            category: "Food  & Beverage"
          },
          {
            title: "Top Quality South African Strelitzia Nicolai Seeds",
            img: "https://alietc.com/cache/medium/product/8910/u8aACJjpwk5wvQrlkqMg.webp",
            category: "Food  & Beverage"
          },
          
          
        ],
        patterns: [
          {
            img: "https://alietc.com/themes/velocity/assets/images/Partners-logo5.webp"
          },
          {
            img: "https://alietc.com/themes/velocity/assets/images/Partners-logo9.webp"
          },
          {
            img: "https://alietc.com/themes/velocity/assets/images/Partners-logo2.webp"
          },
          {
            img: "https://alietc.com/themes/velocity/assets/images/Partners-logo5.webp"
          },
          {
            img: "https://alietc.com/themes/velocity/assets/images/Partners-logo9.webp"
          },
          {
            img: "https://alietc.com/themes/velocity/assets/images/Partners-logo2.webp"
          },
          {
            img: "https://alietc.com/themes/velocity/assets/images/Partners-logo5.webp"
          },
          {
            img: "https://alietc.com/themes/velocity/assets/images/Partners-logo9.webp"
          },
          {
            img: "https://alietc.com/themes/velocity/assets/images/Partners-logo2.webp"
          },
          {
            img: "https://alietc.com/themes/velocity/assets/images/Partners-logo5.webp"
          },
          {
            img: "https://alietc.com/themes/velocity/assets/images/Partners-logo9.webp"
          },
          {
            img: "https://alietc.com/themes/velocity/assets/images/Partners-logo2.webp"
          },
          {
            img: "https://alietc.com/themes/velocity/assets/images/Partners-logo5.webp"
          },
          {
            img: "https://alietc.com/themes/velocity/assets/images/Partners-logo9.webp"
          },
          {
            img: "https://alietc.com/themes/velocity/assets/images/Partners-logo2.webp"
          },
          {
            img: "https://alietc.com/themes/velocity/assets/images/Partners-logo5.webp"
          },
          {
            img: "https://alietc.com/themes/velocity/assets/images/Partners-logo9.webp"
          },
          {
            img: "https://alietc.com/themes/velocity/assets/images/Partners-logo2.webp"
          },
          
        ],
        news: [
          {
            img: "https://alietc.com/storage/blog/841/iHsSo0aQFQND7Rm0lf8I.webp",
            title: "United Calls off Flights as Crew's Covid Cases Grow",
            text: "There has been a limit in the U.S. Airlines’ timetables since the end of 2021 due to spread of Omicron.",
            data: " on January 12, 2022"
          },
          {
            img: "https://alietc.com/storage/blog/842/7H9HeIMVGWHg57wABKiR.webp",
            title: "Test To Blog",
            text: "There has been a limit in the U.S. Airlines’ timetables since the end of 2021 due to spread of Omicron.",
            data: " on January 12, 2022"
          },
          {
            img: "https://alietc.com/storage/blog/841/iHsSo0aQFQND7Rm0lf8I.webp",
            title: "United Calls off Flights as Crew's Covid Cases Grow",
            text: "There has been a limit in the U.S. Airlines’ timetables since the end of 2021 due to spread of Omicron.",
            data: " on January 12, 2022"
          },
          {
            img: "https://alietc.com/storage/blog/842/7H9HeIMVGWHg57wABKiR.webp",
            title: "Test To Blog",
            text: "There has been a limit in the U.S. Airlines’ timetables since the end of 2021 due to spread of Omicron.",
            data: " on January 12, 2022"
          },
          {
            img: "https://alietc.com/storage/blog/841/iHsSo0aQFQND7Rm0lf8I.webp",
            title: "United Calls off Flights as Crew's Covid Cases Grow",
            text: "There has been a limit in the U.S. Airlines’ timetables since the end of 2021 due to spread of Omicron.",
            data: " on January 12, 2022"
          },
          {
            img: "https://alietc.com/storage/blog/842/7H9HeIMVGWHg57wABKiR.webp",
            title: "Test To Blog",
            text: "There has been a limit in the U.S. Airlines’ timetables since the end of 2021 due to spread of Omicron.",
            data: " on January 12, 2022"
          },
        ],
        settings: {
          "arrows": true,
          "dots": false,
          "infinite": true,
          "initialSlide": 2,
          "speed": 500,
          "slidesToShow": 4,
          "slidesToScroll": 1,
          "swipeToSlide": true,
          "useCSS": true
        },
        settings2: {
          "arrows": true,
          "autoplay": true,
          "dots": false,
          "infinite": true,
          "initialSlide": 2,
          "speed": 300,
          "slidesToShow": 6,
          "slidesToScroll": 1,
          "swipeToSlide": true,
          "useCSS": true
        },
        settings3: {
          "arrows": false,
          "autoplay": true,
          "dots": false,
          "infinite": true,
          "initialSlide": 2,
          "speed": 150,
          "slidesToShow": 2,
          "slidesToScroll": 1,
          "swipeToSlide": true,
          "useCSS": true
        }
      }
    },
    computed: {
      rate() {
        console.log(2222);
        return this.feature_Products.slice(0,3)
      }
    }
  }
</script>

<style scoped>
.categories-wrapper {
  border: 1px solid #ededed;
  margin-top: 60px;
}
.category-col {
  border-left: 1px solid #ededed;
  border-bottom: 1px solid #ededed;
}

/* popular-category */
  .title {
    font-size: 24px;
    font-weight: 700;
    margin-bottom: 60px; 
  }
.popular-category {
  position: relative;
  background-color: #f6f6f6;
  margin-top: 60px;
  padding: 10px 10px 64px;
  -webkit-box-shadow: inset 0 1px 5px rgb(0 0 0 / 8%);
  box-shadow: inset 0 1px 5px rgb(0 0 0 / 8%);
}
.category_item {
  margin-bottom: 20px;
}
/* Product */
.product-row {
  margin-top: 60px;
}
.product-title {
  border-bottom: 2px solid #ebebeb;
  margin-bottom: 20px;
  padding-bottom: 10px;
  font-weight: 700;
  font-size: 20px;
  text-align: left;
}

/* forma */
.form-row {
  margin-top: 40px;
  margin-bottom: 60px;
  position: relative;
  padding: 40px;
}
.form-row::before {
  border-radius: 3px;
  /* z-index: -1; */
  position: absolute;
  content: "";
  display: block;
  width: 100%;
  height: 100%;
  left: 0;
  top: 0;
  background: linear-gradient(90deg,rgba(26,26,26,.98) 25%,rgba(26,26,26,0) 90%), url("../assets/img/form.webp");
}
.form-left, .form-right {
  z-index: 2;
}
.form-left div{
  width: 75%;
  margin: 0 auto;
  color: #fff;
}
.form-left_title {
  margin-top: 30px;
}
.form-left_text {
  font-size: 15px;
}
.form-right {
  padding-right: 40px;
}
.form-right span {
  display: block;
  font-size: 16px;
  font-weight: bold;
  padding: 7px;
  margin-bottom: 20px;
  border-radius: 5px;
  background-color: #f57a1d;
  color: #fff;
}
.form_form {
}
.form_form_input {
  margin-bottom: 20px;
}
.form_form_input .form-control {
  width: 32%;
}
::placeholder {
  font-size: 15px;
  font-weight: 400;
  line-height: 1.5;
}
.form-floating .form-control {
  height: auto;
}
.form-floating label{
  font-size: 15px;
  font-weight: 400;
  line-height: 1.5;
}
.button {
  text-align: left;
  margin-top: 20px;
}
.button button {
  padding: 10px 20px;
  font-weight: 600;
  font-size: 15px;
  font-family: 'Roboto Condensed',sans-serif;
  color: #fff;
  border-radius: 4px;
  background-color: #f57a1d;
  border: none;
}
.our-pattern {
  margin-bottom: 60px;
}
.news-row {
  margin-bottom: 60px;
}

.product-item + .product-item{
  margin-top: 20px;
}
</style>