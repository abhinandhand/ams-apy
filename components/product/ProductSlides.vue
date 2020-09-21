<template>
  <div>
    <div class="slides-list">
      <div class=" brand-slide item-1">
        <div class="slide-1"></div>
      <div class="slide-color"></div>
      <div class="slide-content">
      <div class="container">
        <div class="row align-items-center">
          <div class="col text-center brand-content">
            <p class="text-capitalize brand-para-prefix">{{$t('family-business')}}</p>
            <p class="text-capitalize brand-para-heading">{{$t('medical-cannabis')}}</p>
            <p class="brand-para-caption">{{$t('we-are-proud')}}</p>
          <div class="buy-now-div d-flex justify-content-center">
            <p class="buy-now-btn">{{$t('buy-now')}}</p>
          </div>
          </div>

        </div>

      </div>
          
      </div>
      </div>
      <!-- <div class=" brand-slide item-2">
<div class="slide-2">

      </div>
      </div> -->
      
    </div>
    
      
  </div>
</template>

<script>
export default {};
</script>

<style lang="scss">
.slides-list {
  position: relative;
  height: 785px;

  @media (max-width: 767px){
    height: 457px;
  }
}
.brand-slide {
  height: inherit;
  position: relative;
}
.slide-1 {
  position: relative;
  //background-image: url(~@/assets/images/screen/slide-1.jpg);
  background-image: url(~@/assets/images/screen/screen1.jpeg);
  background-size: cover;
  height: inherit;
  // background-position: 0 -41px;
  background-repeat: no-repeat;
}
.slide-2 {
  position: relative;
  background-image: url(~@/assets/images/screen/slide-2.jpg);
  background-size: cover;
  height: 785px;
  background-position: 0 -41px;
  background-repeat: no-repeat;
}
.slide-color {
  background-color: rgba(20, 29, 40, 0.65);
  background-image: none;
  position: absolute;
  height: 100%;
  width: 100%;
  top: 0;
  left: 0;
}
.slide-content {
  color: white;
  position: absolute;
  top: 0;
  width: 100%;
}
.brand-content {
  padding-top: 160px;
  padding-bottom: 260px;
  @media (max-width: 767px){
    padding-top: 100px;
  padding-bottom: 200px;
  }
}
.brand-para-prefix {
  font-weight: bold;
  margin: 0;
}
.brand-para-heading {
  font-size: 85px;
  font-weight: 600;
  line-height: 85px;
  margin: 20px 0px 0px 0px;

  @media (max-width: 991px) and (min-width: 768px){
    font-size: 50px;
    line-height: 50px;
  }
  @media (max-width: 767px){
    font-size: 35px;
    line-height: 35px;
  }
}
.brand-para-caption {
  color: rgb(7, 157, 102);
  font-size: 20px;
  font-weight: 500;
  margin-top: 44px;

  @media (max-width: 767px){
    margin-top: 32px;
    font-size: 16px;
  }
}
.buy-now-div{
  margin-top: 40px;
}
.buy-now-btn {
  cursor: pointer;
  width: 180px;
  font-family: Poppins, sans-serif;
  font-size: 16px;
  line-height: 1;
  font-weight: 500;
  letter-spacing: 0;
  color: rgba(255, 255, 255, 1);
  border-color: rgba(255, 255, 255, 1);
  background-color: rgba(35, 157, 219, 0);
  background-image: none;
  border-width: 2px;
  border-style: solid;
  padding-top: 14px;
  padding-right: 42px;
  padding-bottom: 14px;
  padding-left: 42px;
  border-radius: 2px;
  box-shadow: none;
}
</style>