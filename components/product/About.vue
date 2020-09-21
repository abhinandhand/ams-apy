<template>
<div id="about-el">
<div class="about-container">
    <div class="container ">
      <div class="about-flex">
          <div class="about-info">
              <div>
                  <div class="info-container">
                        <p class="about-suffix-title"><span>{{$t('about.title')}}</span></p>
                        <p class="about-heading"><span>{{$t('about.why-choose')}}</span></p>
                        <p class="desc-1"><span>{{$t('about.why-choose-desc-para1')}}</span></p>
                        <p class="desc-2"><span>{{$t('about.why-choose-desc-para2')}}</span></p>

                        <p class="about-heading-2"><span>{{$t('about.making-our-product')}}</span></p>
                        <p class="desc-1"><span>{{$t('about.making-para1')}}</span></p>
                        <p class="desc-2"><span>{{$t('about.making-para2')}}</span></p>

                  </div>
              </div>
          </div>
          <div class="about-image">
              <div class="div-img-set">
                  <picture >
                      <source srcset="http://cannabias.themily.com/wp-content/uploads/brizy/8208/assets/images/iW=490&amp;iH=538&amp;oX=0&amp;oY=0&amp;cW=490&amp;cH=538/image_286.png 1x, http://cannabias.themily.com/wp-content/uploads/brizy/8208/assets/images/iW=980&amp;iH=1076&amp;oX=0&amp;oY=0&amp;cW=980&amp;cH=1076/image_286.png 2x" media="(min-width: 992px)">
                      <source srcset="http://cannabias.themily.com/wp-content/uploads/brizy/8208/assets/images/iW=298&amp;iH=327&amp;oX=0&amp;oY=0&amp;cW=298&amp;cH=327/image_286.png 1x, http://cannabias.themily.com/wp-content/uploads/brizy/8208/assets/images/iW=596&amp;iH=654&amp;oX=0&amp;oY=0&amp;cW=596&amp;cH=654/image_286.png 2x" media="(min-width: 768px)">
                      <img alt="" class="brz-img" src="http://cannabias.themily.com/wp-content/uploads/brizy/8208/assets/images/iW=400&amp;iH=439&amp;oX=0&amp;oY=0&amp;cW=400&amp;cH=439/image_286.png" srcset="http://cannabias.themily.com/wp-content/uploads/brizy/8208/assets/images/iW=400&amp;iH=439&amp;oX=0&amp;oY=0&amp;cW=400&amp;cH=439/image_286.png 1x, http://cannabias.themily.com/wp-content/uploads/brizy/8208/assets/images/iW=800&amp;iH=878&amp;oX=0&amp;oY=0&amp;cW=800&amp;cH=878/image_286.png 2x">
                      </picture>
              </div>
          </div>
      <div>

      </div>
      </div>
      <div class="buy-now-div-about">
            <p class="buy-now-btn-about">{{$t('buy-now')}}</p>
          </div>
    </div>

</div>
</div>
</template>

<script>
export default {};
</script>

<style lang="scss">
.about-container{
    padding: 45px 0px;
    background-color: #ffffff;
    @media (min-width: 992px){
    padding: 0px 15px 40px;
    }
    @media (max-width: 767px){
    padding: 60px 0px;
   }
}
.info-container {
 padding: 100px 0px 0px 0px;
 @media (max-width: 767px){
    padding: 0px;
    text-align: center;
    margin: 30px 0px;
   }
}
.about-flex{
    display: flex;
    flex-direction: row;
    padding: 45px 0px;
    flex-wrap: wrap !important;
    @media (max-width: 767px){
    flex-direction: column-reverse;
    padding: 0px 0px;
    flex-wrap: unset !important;
    }
}
.about-info{
    @media (min-width: 992px){
    will-change: flex, max-width;
    flex: 1 1 55.6%;
    max-width: 55.6%;
    -webkit-flex: 1 1 55.6%;
}
    @media (min-width: 767px) and (max-width: 992px){
    will-change: flex, max-width;
    flex: 1 1 55%;
    max-width: 55%;
    -webkit-flex: 1 1 55%;
   }
    @media (max-width: 767px) {
    will-change: flex, max-width;
    flex: 1 1 100%;
    max-width: 100%;
    -webkit-flex: 1 1 100%;
    }
    
}
.about-image{
    will-change: flex, max-width;
    flex: 1 1 44.4%;
    max-width: 44.4%;
    -webkit-flex: 1 1 44.4%;

    @media (max-width: 767px) {
    will-change: flex, max-width;
    flex: 1 1 100%;
    max-width: 100%;
    -webkit-flex: 1 1 100%;
}
}
.about-image .div-img-set picture{
    width: 100%;
    height: auto;
}

.brz-img{
    max-width: 100%;
    width: 100%;
}
.about-suffix-title{
    color: #079d66;
    font-weight: 600 !important;
    margin-bottom: 10px;
}
.about-heading {
    font-family: Montserrat, sans-serif;
    font-size: 30px;
    font-weight: 700;
    letter-spacing: -1px;
    line-height: 1em;
    margin-bottom: 0px;

    @media (max-width: 767px) {
    font-size: 22px;
    font-weight: 700;
    letter-spacing: 0px;
    line-height: 1em;
   }
}
.about-heading-2 {
    font-family: Montserrat, sans-serif;
    font-size: 30px;
    font-weight: 700;
    letter-spacing: -1px;
    line-height: 1em;
    margin-bottom: 0px;
    margin-top: 35px;

    @media (max-width: 767px) {
    font-size: 22px;
    font-weight: 700;
    letter-spacing: 0px;
    line-height: 1em;
   }
}
.desc-1{
    margin-top: 30px !important;
    font-family: Poppins, sans-serif;
    font-size: 16px;
    font-weight: 300;
    letter-spacing: 0px;
    line-height: 1.5em;
    color: #5c6f87;
}

.desc-2{
    margin-top: 20px !important;
    font-family: Poppins, sans-serif;
    font-size: 16px;
    font-weight: 300;
    letter-spacing: 0px;
    line-height: 1.5em;
    color: #5c6f87;
}

.buy-now-div-about{
  text-align: center;
  @media (max-width: 767px) {
    margin-top: 30px;
    display: flex;
    justify-content: center;
   }
}
.buy-now-btn-about {
  cursor: pointer;
  width: 180px;
  font-family: Poppins, sans-serif;
  font-size: 16px;
  line-height: 1;
  font-weight: 500;
  letter-spacing: 0;
  text-align: center;
  color: rgba(20, 29, 40, 1);
  border-color: rgba(7, 157, 102, 1);
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
  margin-bottom: 0px;
}

</style>