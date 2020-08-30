<template>
  <div id="header" class="header-bg">
    <div class="container">
      <div class="row align-items-center pt-3 pb-3">
        <div class="col-xl-4 col-lg-6 text-center text-lg-left fw-300">
          <span class="pr-3"
            ><i class="fa fa-phone pr-2 "></i
            ><a href="tel:010-31-643851275">010-31-643851275</a></span
          >
        </div>
        <div class="col-lg-4 text-center hidden-below-xl">
          <a href="" rel="home" class="logo logo_image_only">
            <img
              width="245px"
              class="logo-color"
              src="~/assets/images/icons/brand-7.svg"
              alt=""
            />
          </a>
        </div>
        <div class="col-xl-4 col-lg-6 text-center text-lg-right mt-2 mt-lg-0">
          <span class="social-icons">
            <span class="social-icons ">
              <a
                href="https://www.facebook.com/robbie.kalloe"
                class="fa fa-facebook mx-3"
              >
                <span class=""></span>
              </a>

              <a href="" class="fa fa-whatsapp mx-3">
                <span class=""></span>
              </a>
              <span>
                <img style="cursor:pointer"
                  v-if="currentLang === 'en'"
                  class="mx-3" @click="changeLanguage('jp')"
                  width="26px"
                  src="~/assets/images/icons/lang-jp.png"
              />
              <img style="cursor:pointer"
                  v-else @click="changeLanguage('en')"
                  class="mx-3"
                  width="26px"
                  src="~/assets/images/icons/lang-en.png"
              />
              </span>
            </span>
          </span>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data(){
    return {
      currentLang: ""
    }
  },
 created(){
  this.currentLang = this.$i18n.locale;
 },
  methods:{
    changeLanguage(value){
      this.$i18n.locale = value;
      this.currentLang = value;
    }
  }
};
</script>

<style lang="scss" scoped>
.header-bg {
  background-color: #141d28;
  color: #ffffff;
}

a {
  color: #ffffff;
}


</style>
 