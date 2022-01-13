<template>
  <header>
    <div class="header-top">
      <div class="container">
        <div class="row align-items-center">
          <div class="col-2 logo-img">
            <img src="../assets/img/logo.webp" alt="Logo img" width="155" height="32">
          </div>
          <div class="col-8 search">
            <form method="Post" class="search-form">
              <input class="search-form_input" type="text" name="product" id="search" v-model="search_product" placeholder="Search products here">
              <button class="search-form_button"></button>
            </form>
          </div>
          <div class="col-2 login d-flex align-items-center justify-content-end">
            <router-link to="#" class="link">
              <svg width="32" height="32"><path d="M23,4c3.9,0,7,3.1,7,7c0,6.3-11.4,15.9-14,16.9C13.4,26.9,2,17.3,2,11c0-3.9,3.1-7,7-7c2.1,0,4.1,1,5.4,2.6l1.6,2l1.6-2
              C18.9,5,20.9,4,23,4 M23,2c-2.8,0-5.4,1.3-7,3.4C14.4,3.3,11.8,2,9,2c-5,0-9,4-9,9c0,8,14,19,16,19s16-11,16-19C32,6,28,2,23,2L23,2
              z"></path></svg>
            </router-link>
            <svg class="profile" width="32" height="32"><path d="M16,18C9.4,18,4,23.4,4,30H2c0-6.2,4-11.5,9.6-13.3C9.4,15.3,8,12.8,8,10c0-4.4,3.6-8,8-8s8,3.6,8,8c0,2.8-1.5,5.3-3.6,6.7
            C26,18.5,30,23.8,30,30h-2C28,23.4,22.6,18,16,18z M22,10c0-3.3-2.7-6-6-6s-6,2.7-6,6s2.7,6,6,6S22,13.3,22,10z"></path></svg>
            <div class="login-register">
              <router-link to="#" class="link sign-in">
                Sign in
              </router-link>
              <router-link to="#" class="link register">
                join Free
              </router-link>
            </div>
          </div>
        </div>
      </div>
    </div>
    <div class="header-bottom">
      <div class="container">
        <div class="row align-items-center">
          <div class="col-3 categories d-flex align-items-center">
            <div class="categoties-button d-flex align-items-center">
              <svg width="16px" height="12px" class="mr-2 categories-img"><path d="M0,7L0,5L16,5L16,7L0,7ZM0,0L16,0L16,2L0,2L0,0ZM12,12L0,12L0,10L12,10L12,12Z"></path></svg>
              <router-link class="link categories-link" to="#">All Categories</router-link>
            </div>
          </div>
          <div class="col-7 d-flex align-items-center links">
            <ul class="features-links d-flex">
              <li class="feature-item" v-for="(link, index) in links" :key="index">
                <router-link class="link feature-link" to="#">{{link}}</router-link>
              </li>
            </ul>
            <div class="dropdown">
                <a class="dropdown-toggle text-decoration-none feature-link " href="#" role="button" id="dropdownMenuLink" data-bs-toggle="dropdown" aria-expanded="false">
                  Learn more
                </a>

                <ul class="dropdown-menu" aria-labelledby="dropdownMenuLink">
                  <li v-for="link in rest" :key="link"><router-link to="#" class="dropdown-item feature-link">{{ link }}</router-link></li>
                </ul>
              </div>
          </div>
          <div class="col-2 d-flex align-items-center">
            <router-link to="#" class="link sms-link">
              <Sms></Sms>
            </router-link>
            <Language></Language>
          </div>
        </div>
      </div>
    </div>
  </header>

</template>

<script>
import Sms from '@/components/Sms.vue';
import Language from '@/components/Language.vue';
  export default {
    components: {
      Sms,
      Language
    },
    data() {
      return {
        search_product: null,
        features: {
          links: ["Home", "Premium Services", "Buyers", "Products", "Countries", "Importer","Suppliers", "Manufactures"]
        }
      }
    },
    computed: {
      links () {
        if(this.features.links.length<6) {
          console.log("true");
          return this.features.links
        }
        else {
          return this.features.links.slice(0,5)
        }
      },
      rest () {
        if(this.features.links.length>=6) {
          return this.features.links.slice(5, this.features.links.length)
        }
        return 0
      }
    }
  }
</script>

<style scoped>
.header-top {
  padding-top: 18px;
  padding-bottom: 18px;
  border-bottom: 1px solid #ededed;
  top: 0;
  z-index: 100;
  position: -webkit-sticky;
  position: sticky;
  background: #fff;
}
.logo-img {
  text-align: left;
}
.search {
  display: flex;
  justify-content: center;
}
.search-form {
  position: relative;
  width: 90%;
}
.search-form_input {
  width: 100%;
  border-color: #ededed;
  background-color: #ededed;
  font-size: 15px;
  border-radius: 0;
  padding: 10px 10px;
  line-height: 20px;
  letter-spacing: 0;
  border: none;
  outline: none;
}
.search-form_button {
  position: absolute;
  right: 8px;
  top: 8px;
  background-image: url("../assets/img/search-icon.png");
  background-size: contain;
  background-repeat: no-repeat;
  width: 25px;
  height: 25px;
  padding: 0;
  margin: 0;
  border: none;
  background-color: transparent;
}
.profile {
  margin-left: 15px;
}
.login-register {
  display: flex;
  flex-direction: column;
  margin-left: 10px;
}
.sign-in {
  color: #b2b3b3;
  font-weight: 400;
  font-size: 13px;
  text-align: left;
}
.register {
  color: #343a40;
  font-size: 18px;
  font-weight: bold;
}
/* header-bottom */
.header-bottom {
  padding-top: 5px;
  padding-bottom: 5px;
}
.categories-img {
  margin-right: 12px;
}
.categories-link {
  font-size: 16px;
  color: #262626;
  font-weight: 600;
}
.features-links {
  padding: 0;
  padding-left: 5px;
  margin: 0;
  list-style-type: none;
  border-left: 1px solid #ededed;
}
.feature-link {
    display: block;
    color: #262626;
    padding: 11px 9px;
    font-size: 15px;
    font-weight: 500;
}
.feature-link:hover {
  color: #f47a1d;
  background-color: #f2f2f2;
}
.sms-link {
  display: block;
  padding-top: 11px;
  padding-bottom: 11px;
  padding-right: 8px;
  border-right: 2px solid rgba(143, 107, 107, 0.4);
}
</style>