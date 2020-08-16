<template>
  <div>
    <link
      rel="stylesheet"
      href="https://stackpath.bootstrapcdn.com/font-awesome/4.7.0/css/font-awesome.min.css"
      integrity="sha384-wvfXpqpZZVQGK6TAh5PVlGOfQNHSoD2xbE+QkPxCAFlNEevoEH3Sl0sibVcOQVnN"
      crossorigin="anonymous"
    />

    <div v-show="!isLoading">
      <Header></Header>
      <Nuxt />
      <h6>footer</h6>
    </div>
    
    <div v-show="isLoading" style="height:100vh">
      <div class="loading-img-div">
        <img src="favicon.ico" alt="" />
      </div>
    </div>
  </div>
</template>
<script>
import Header from "@/components/templates//Header.vue";

export default {
  components: {
    Header
  },
  data() {
    return {
      isLoading: true
    };
  },
  mounted() {
    setTimeout(() => {
      this.isLoading = false;
    }, 500);
  }
};
</script>

<style>
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
