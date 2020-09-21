<template>
<div id="benefits-el">
<div class="benefits-container">
    <div class="container ">
      <div class="benefits-flex">
          <div class="benefits-info">
              <div>
                  <div class="benefit-info-container">
                        <p class="benefits-suffix-title"><span>{{$t('benefit.title')}}</span></p>
                        <p class="benefits-heading"><span>{{$t('benefit.uses')}}</span></p>
                        <p class="desc-1"><span>{{$t('benefit.uses-desc1')}}</span></p>
                        <p class="desc-2"><span>{{$t('benefit.uses-desc2')}}</span></p>

                        <p class="benefits-heading head2"><span>{{$t('benefit.positive-effects')}}</span></p>
                        <div id="benefit-list">
                        <div class="benefit-item">
                            <p class="list-heading">1. {{$t('benefit.neuro')}}</p>
                            <p class="list-desc">{{$t('benefit.neuro-desc1')}}</p>
                            <p class="list-desc">{{$t('benefit.neuro-desc2')}}</p>
                             <a target="_blank" style="text-decoration:none" href="https://pubmed.ncbi.nlm.nih.gov/28538134/">
                            <div class="facts-div">
                                 <p class="facts-btn">{{$t('benefit.studies')}}</p>
                            </div>
                            </a>
                        </div>
                        </div>

                  </div>
              </div>
                  
          </div>
          <div class="benefits-image">
              <div class="div-img-set">
                  <picture >
                      <img alt="" class="brz-img" src="~/assets/images/screen/product.jpg">
                    </picture>
              </div>
          </div>
      <div>

      </div>
      </div>
      <div class="benefit-list2">
            <div class="row">
                <div class="col-md-6 col-sm-12">
                    <div class="benefit-item">
                            <p class="list-heading">2. {{$t('benefit.relieves')}}</p>
                            <p class="list-desc">{{$t('benefit.relieves-desc1')}}</p>
                            <p class="list-desc">{{$t('benefit.relieves-desc2')}}</p>
                             <a target="_blank" style="text-decoration:none" href="https://www.ncbi.nlm.nih.gov/pmc/articles/PMC5922297/">
                            <div class="facts-div">
                                 <p class="facts-btn">{{$t('benefit.studies')}}</p>
                            </div>
                            </a>
                    </div>
                </div>
                <div class="col-md-6 col-sm-12">
                    <div class="benefit-item">
                            <p class="list-heading">3. {{$t('benefit.heart-health')}}</p>
                            <p class="list-desc">{{$t('benefit.heart-desc')}}</p>
                             <a target="_blank" style="text-decoration:none" href="https://www.ncbi.nlm.nih.gov/pmc/articles/PMC5470879/">
                            <div class="facts-div">
                                 <p class="facts-btn">{{$t('benefit.studies')}}</p>
                            </div>
                            </a>
                    </div>
                </div>
            </div>
            
            <div class="row">
                
                <div class="col-md-6 col-sm-12">
                    <div class="benefit-item">
                            <p class="list-heading">4. {{$t('benefit.acne')}}</p>
                            <p class="list-desc">{{$t('benefit.acne-desc')}}</p>
                             <a target="_blank" style="text-decoration:none" href="https://www.ncbi.nlm.nih.gov/pmc/articles/PMC3780801/">
                            <div class="facts-div">
                                 <p class="facts-btn">{{$t('benefit.studies')}}</p>
                            </div>
                            </a>
                    </div>
                </div>
                <div class="col-md-6 col-sm-12">
                    <div class="benefit-item">
                            <p class="list-heading">5. {{$t('benefit.cancer-symptoms')}}</p>
                            <p class="list-desc">{{$t('benefit.cancer-desc')}}</p>
                             <a target="_blank" style="text-decoration:none" href="https://pubmed.ncbi.nlm.nih.gov/21566064/">
                            <div class="facts-div">
                                 <p class="facts-btn">{{$t('benefit.studies')}}</p>
                            </div>
                            </a>
                    </div>
                </div>
            </div>
                <div >
                    <div class="benefit-item">
                            <p class="list-heading">6. {{$t('benefit.several-others')}}</p>
                            <div class="other-items">
                                <p class="list-desc">
                                <span class="desc-heading">{{$t('benefit.other1')}}: </span>
                                {{$t('benefit.other-desc1')}}
                            </p>
                             <a target="_blank" style="text-decoration:none" href="https://pubmed.ncbi.nlm.nih.gov/25667194/">
                            <div class="facts-div-others">
                                 <p class="facts-btn">{{$t('benefit.studies')}}</p>
                            </div>
                            </a>
                            </div>
                            <div class="other-items">
                                <p class="list-desc">
                                <span class="desc-heading">{{$t('benefit.other2')}}: </span>
                                {{$t('benefit.other-desc2')}}
                            </p>
                             <a target="_blank" style="text-decoration:none" href="https://www.ncbi.nlm.nih.gov/pmc/articles/PMC4444130/">
                            <div class="facts-div-others">
                                 <p class="facts-btn">{{$t('benefit.studies')}}</p>
                            </div>
                            </a>
                            </div>
                            <div class="other-items">
                                <p class="list-desc">
                                <span class="desc-heading">{{$t('benefit.other3')}}: </span>
                                {{$t('benefit.other-desc3')}}
                            </p>
                             <a target="_blank" style="text-decoration:none" href="https://pubmed.ncbi.nlm.nih.gov/25916739/">
                            <div class="facts-div-others">
                                 <p class="facts-btn">{{$t('benefit.studies')}}</p>
                            </div>
                            </a>
                            </div>
                            <div class="other-items">
                                <p class="list-desc">
                                <span class="desc-heading">{{$t('benefit.other4')}}: </span>
                                {{$t('benefit.other-desc4')}}
                            </p>
                             <a target="_blank" style="text-decoration:none" href="https://pubmed.ncbi.nlm.nih.gov/16698671/">
                            <div class="facts-div-others">
                                 <p class="facts-btn">{{$t('benefit.studies')}}</p>
                            </div>
                            </a>
                            </div>
                    </div>
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
.benefits-container {
  padding: 45px 0px;
  background-color: #ffffff;
  @media (min-width: 992px) {
    padding: 0px 15px 40px;
  }
  @media (max-width: 767px) {
    padding: 60px 0px;
  }
}
.benefit-info-container {
  padding: 0px 0px 0px 0px;
  @media (max-width: 767px) {
    padding: 40px 0px 0px;
  }
}
.benefits-container {
  padding: 0px;
  @media (max-width: 767px) {
    padding-top: 30px;
    text-align: center;
    margin: 30px 0px;
  }
}
.benefits-flex {
  display: flex;
  flex-direction: row;
  padding: 45px 0px 0px;
  flex-wrap: wrap !important;
  @media (max-width: 767px) {
    flex-direction: column-reverse;
    padding: 0px 0px;
    flex-wrap: unset !important;
  }
}
.benefits-info {
  @media (min-width: 992px) {
    will-change: flex, max-width;
    flex: 1 1 65.6%;
    max-width: 65.6%;
    -webkit-flex: 1 1 65.6%;
    padding-right: 18px;
  }
  @media (min-width: 767px) and (max-width: 992px) {
    will-change: flex, max-width;
    flex: 1 1 65%;
    max-width: 65%;
    -webkit-flex: 1 1 65%;
  }
  @media (max-width: 767px) {
    will-change: flex, max-width;
    flex: 1 1 100%;
    max-width: 100%;
    -webkit-flex: 1 1 100%;
  }
}
.benefits-image {
  will-change: flex, max-width;
  flex: 1 1 34.4%;
  max-width: 34.4%;
  -webkit-flex: 1 1 34.4%;

  @media (max-width: 767px) {
    will-change: flex, max-width;
    flex: 1 1 100%;
    max-width: 100%;
    -webkit-flex: 1 1 100%;
  }
}
.benefits-image .div-img-set picture {
  width: 100%;
  height: auto;
}

.brz-img {
  max-width: 100%;
  width: 100%;
  border-radius: 8px;
}
.benefits-suffix-title {
  color: #079d66;
  font-weight: 600 !important;
  margin-bottom: 10px;
}
.benefits-heading {
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
.benefits-heading-2 {
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
.benefit-item{
    padding-bottom:40px ;
}
.desc-1 {
  margin-top: 30px !important;
  font-family: Poppins, sans-serif;
  font-size: 16px;
  font-weight: 300;
  letter-spacing: 0px;
  line-height: 1.5em;
  color: #5c6f87;
}

.desc-2 {
  margin-top: 20px !important;
  font-family: Poppins, sans-serif;
  font-size: 16px;
  font-weight: 300;
  letter-spacing: 0px;
  line-height: 1.5em;
  color: #5c6f87;
}

.facts-div {
  text-align: center;
  @media (max-width: 767px) {
    margin-top: 30px;
    display: flex;
    justify-content: center;
  }
}
.facts-btn {
  cursor: pointer;
    width: 216px;
    font-family: Poppins, sans-serif;
    font-size: 16px;
    line-height: 1;
    font-weight: 500;
    letter-spacing: 0;
    text-align: center;
    color: #141d28;
    border-color: #079d66;
    background-color: rgba(35, 157, 219, 0);
    background-image: none;
    border-width: 2px;
    border-style: solid;
    padding-top: 16px;
    padding-right: 38px;
    padding-bottom: 16px;
    padding-left: 38px;
    border-radius: 2px;
    box-shadow: none;
    margin-bottom: 0px;
}
#benefit-list{
    padding: 30px 0px 0px;
    @media (max-width: 767px) {
        padding: 30px 0px 0px;
  }
}
.list-heading{
    font-family: Montserrat, sans-serif;
    font-size: 30px;
    font-weight: 500;
    letter-spacing: -1px;
    line-height: 1em;
    color: #079d66;

  @media (max-width: 767px) {
    font-size: 22px;
    font-weight: 500;
    letter-spacing: 0px;
    line-height: 1em;
  }
}

.list-desc{
    margin-top: 10px !important;
    font-family: Poppins, sans-serif;
    font-size: 16px;
    font-weight: 300;
    letter-spacing: 0px;
    line-height: 1.5em;
    color: #5c6f87;
}
.desc-heading{
    font-weight: 500;
}
.other-items{
    margin-bottom: 30px;
}
.head2{
  margin-top: 40px;
    @media (max-width: 767px) {
    
        margin-top: 50px;
  }
}
.list-head1{
    @media (max-width: 767px) {
    
        margin-top: 40px;
  }
}
.facts-div-others{
    text-align: center;
  @media (max-width: 767px) {
    margin-top: 20px;
    display: flex;
    justify-content: center;
  }
}
</style>