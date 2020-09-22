<template>
  <div id="contacts-el">
      <footer class="ams-footer">
          <div class="container footer-container">
              <div class="row">
                  <div class="col-md-4 col-sm-12 foot-col">
                      <div class="img-brand-footer">
                          <a href="" rel="home" class="logo logo_image_only">
                            <img width="245px" class="logo-color" src="~/assets/images/icons/brand-7.svg" alt=""/>
                          </a>
                      </div>
                    <p class="footer-caption">{{$t('footer.caption1')}}</p>
                    <p>{{$t('footer.caption2')}}</p>
                  </div>
                  <div class="col-md-4 col-sm-12 foot-col">
                      <p class="footer-heading">{{$t('menus.contact')}}</p>
                  </div>
                  <div class="col-md-4 col-sm-12 foot-col">
                      <p class="footer-heading">{{$t('footer.subscribe')}}</p>
                  </div>
              </div>
          </div>
      </footer>
      <div class="copyright">
          <div class="col-sm-12 text-center copy-div">
				<div class="footer-md">
                    © Amsterdam Apotheacry <span class="copyright_year">&nbsp;2020 &nbsp;</span>| Created with 
                    <i class="fa fa-heart color-main"></i>			</div>
               
               <div class="footer-sm">
                     <div>
                         © Amsterdam Apotheacry <span class="copyright_year">2020</span>
                     </div>
                     <div style="    margin-top: 4px;">
                    Created with 
                    <i class="fa fa-heart color-main"></i>
                     </div>
                    			</div>
                </div> 
                 
                </div> 
      </div>
  </div>
</template>

<script>
export default {

}
</script>

<style lang="scss">
.ams-footer{
    background-color: #141d28;
    color: #fff;
}
.footer-container{
    padding: 100px 0px;
    @media (max-width: 767px) {
    padding: 60px 0px;
    }
}
.footer-md{
    display: block;
    @media (max-width: 767px) {
    display: none;
    }
}
.footer-sm{
    display: none;
    @media (max-width: 767px) {
    display: block;
    }
}
.foot-col {
    @media (max-width: 767px) {
    text-align:center;
    margin-bottom: 30px;
    }
}
.foot-col p{
    @media (max-width: 767px) {
    padding: 0px 18px;
    
    }
        
}
.img-brand-footer{
    margin-bottom: 30px;
}
.copyright{
    font-size: 12px;
    color: #fff;
    font-weight: 300;
    text-transform: uppercase;
    letter-spacing: 4px;
    line-height: 1;
    background-color: #233142;
    height: 52px;
}
.copy-div{
    display: flex;
    justify-content: center;
    align-items: center;
    height: inherit;
}
.footer-heading{
    font-size: 30px;
    font-weight: 400;
    margin-bottom: 45px;
    color: #079d66;
    font-family: 'Montserrat', sans-serif;
}

.color-main{
    color: #079d66;
}
</style>