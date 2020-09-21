<template>
  <div>
    <div id="feature-container"  >
      <div class="feature-img item-1" >
        <div class="img-leaves"></div>
      <div class="leaf-color"></div>
      <div class="feature-content" ref="featureContent">
      <div class="container special-conatiner" >
        <div class="row" >
          <div class="col-md-3 col-sm-12  special-content" >
            <div >
                <p class="feature-heading">{{$t('feature.specially')}}</p>
                <p class="feature-desc">{{$t('feature.specially-desc')}}</p>
            </div>
          </div>
          <div class="col-md-3 col-sm-12 special-content" >
             <div>
                <p class="feature-heading">{{$t('feature.form')}}</p>
                <p class="feature-desc pt-1">{{$t('feature.form-desc1')}}</p>
                <p class="feature-desc">{{$t('feature.form-desc2')}}</p>
            </div>
          </div>
          <div class="col-md-3 col-sm-12 special-content" >
            <div>
                <p class="feature-heading">{{$t('feature.quality')}}</p>
                <p class="feature-desc">{{$t('feature.quality-desc')}}</p>
            </div>
          </div>
          <div class="col-md-3 col-sm-12 special-content" >
            <div>
                <p class="feature-heading">{{$t('feature.results')}}</p>
                <p class="feature-desc pt-1">{{$t('feature.results-desc1')}}</p>
                <p class="feature-desc pt-1">{{$t('feature.results-desc2')}}</p>
                <p class="feature-desc pt-1">{{$t('feature.results-desc3')}}</p>
                <p class="feature-desc">{{$t('feature.results-desc4')}}</p>
            </div>
          </div>
        </div>
      </div> 
      </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
    mounted(){
        this.setConatinerHeight();
    },
    methods:{
        setConatinerHeight(){
            console.log(this.$refs.featureContent.clientHeight);
            document.getElementById('feature-container').style.height = this.getHeight(this.$refs.featureContent)+'px';
            //document.getElementById('feature-container').style.height = this.$refs.featureContent.offsetHeight+'px';
        },
        getHeight(element){
        console.log(element)
        element.style.visibility = "hidden";
        document.body.appendChild(element);
        var height = element.offsetHeight + 0;
        document.body.removeChild(element);
        element.style.visibility = "visible";
        document.getElementById('feature-container').appendChild(element);
        return height;
        }
    }
};
</script>

<style lang="scss">
#feature-container{
    position: relative;
}
.feature-img {
  height: inherit;
  position: relative;
}
.img-leaves {
  position: relative;
  background-image: url(~@/assets/images/screen/leaves.jpg);
  background-size: cover;
  height: inherit;
  background-repeat: no-repeat;
  background-position: 50% 50%;
  background-attachment: fixed;
  @media (max-width: 768px){
    background-position: 50% 50%;
    background-attachment:unset;
    background-repeat: repeat;
  }

}
.leaf-color {
  background-color: rgba(20, 29, 40, 0.65);
  background-image: none;
  height: 100%;
  width: 100%;
  position: absolute;
  top: 0;
  left: 0;
}
.feature-content {
  color: white;
  position: absolute;
  top: 0;
  width: 100%;
  overflow: overlay;
}
.special-conatiner{
    padding: 90px 0px;
    @media (max-width: 768px){
    padding: 90px 15px;
  }
}
.feature-heading{
    font-family: Montserrat, sans-serif;
    font-size: 20px;
    font-weight: 700;
    letter-spacing: -1px;
    line-height: 1em;
    margin-bottom: 20px;
    text-align: center;
    
}
.feature-desc{
    font-family: Poppins, sans-serif;
    font-size: 16px;
    font-weight: 300;
    letter-spacing: 0px;
    line-height: 1.5em;
    text-align: center;
    margin-bottom: 0px;
}
.special-content{
    @media (max-width: 768px){
    margin-bottom: 35px;
  }
}

</style>