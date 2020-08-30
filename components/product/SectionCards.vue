<template>
<div class="section-cards-container">
<div class="container cards-container">
      <div class="row align-items-center">
      <div class="cards-item cards-item-margin col-md-4 col-sm-12 text-center">
          <div>
              <picture>
                  <source srcset="~/assets/images/icons/manufact-sm.jpg" media="(min-width: 992px)">
                  <source srcset="~/assets/images/icons/manufact-lg.jpg" media="(min-width: 768px)">
                  <img alt="" class="img-fluid" src="~/assets/images/icons/manufact-lg.jpg" srcset="~/assets/images/icons/manufact-lg.jpg">
              </picture>
                <div class="img-caption">
                    <p class="img-caption-para">{{$t('product-manu')}}</p>
                </div>
          </div>
      </div>
      <div class="cards-item cards-item-margin col-md-4 col-sm-12 text-center">
          <picture>
                  <source srcset="~/assets/images/icons/health-sm.png" media="(min-width: 992px)">
                  <source srcset="~/assets/images/icons/health-lg.jpg" media="(min-width: 768px)">
                  <img alt="" class="img-fluid" src="~/assets/images/icons/health-sm.png" srcset="~/assets/images/icons/health-lg.jpg">
          </picture>
              <div class="img-caption">
                  <p class="img-caption-para">{{$t('benefits')}}</p>
                </div>
      </div>
      <div class="cards-item col-md-4 col-sm-12 text-center">
          <picture>
                  <source srcset="~/assets/images/icons/lab-sm.jpg" media="(min-width: 992px)">
                  <source srcset="~/assets/images/icons/lab-lg.jpg" media="(min-width: 768px)">
                  <img alt="" class="img-fluid" src="~/assets/images/icons/lab-lg.jpg" srcset="~/assets/images/icons/lab-lg.jpg">
          </picture>
              <div class="img-caption">
                  <p class="img-caption-para">{{$t('test-labs')}}</p>
                </div>
      </div>
      </div>
  </div>
</div>
</template>

<script>
export default {};
</script>

<style lang="scss">
.section-cards-container{
    padding: 60px 15px;
    background-color: rgba(238, 240, 242, 1);
    @media (min-width: 992px){
    padding: 0px 15px 60px;
    }
    @media (max-width: 767px){
    padding: 60px 0px;
   }
    
}
.cards-container{
    @media (min-width: 992px){
    margin-top: -90px;
    }
}
.img-caption{
    height: 60px;
    background-color: white;
}
.cards-item{
    cursor: pointer;
}
.cards-item-margin{
    @media (max-width: 767px){
    margin-bottom: 30px;
   }
}
.img-caption{
    display: flex;
    justify-content: center;
    align-items: center;
}
.img-caption-para{
    margin: 0;
    font-size: 19px;
    font-weight: 700;
    letter-spacing: 0px;
    line-height: 1em;
}

</style>