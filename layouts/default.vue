<template>
  <div id="layout-body">
    <link
      rel="stylesheet"
      href="https://stackpath.bootstrapcdn.com/font-awesome/4.7.0/css/font-awesome.min.css"
      integrity="sha384-wvfXpqpZZVQGK6TAh5PVlGOfQNHSoD2xbE+QkPxCAFlNEevoEH3Sl0sibVcOQVnN"
      crossorigin="anonymous"
    />

    <div v-show="!isLoading" class="layout">
      <Header></Header>
      <Menubar/>
      <Nuxt />
      <Footer/>
    </div>
    
    <div v-show="isLoading" style="height:100vh">
      <div class="loading-img-div">
        <img src="favicon.ico" alt="" />
      </div>
    </div>
  </div>
</template>
<script>
import Header from "@/components/templates/Header.vue";
import Footer from '@/components/templates/Footer.vue';
import Menubar from '@/components/templates/Menubar.vue';
export default {
  components: {
    Header,
    Menubar,
    Footer
  },
  data() {
    return {
      isLoading: true
    };
  },
  mounted() {
    setTimeout(() => {
      this.isLoading = false;
    }, 2000);
  }
};
</script>

<style>
.layout{
      transition: 0.5s ease-in-out;
}
.loading-img-div {
  height: 100%;
  display: flex;
  justify-content: center;
  align-items: center;
  background: #f5f5f5;
}
@keyframes zoominoutsinglefeatured {
  0% {
    transform: scale(1, 1);
  }
  50% {
    transform: scale(1.2, 1.2);
  }
  100% {
    transform: scale(1, 1);
  }
}

.loading-img-div img {
  animation: zoominoutsinglefeatured 1s infinite;
}
</style>
