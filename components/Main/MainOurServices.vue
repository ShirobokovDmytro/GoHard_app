<template>
  <section class="our__services">
    <div class="our__services__container">
      <div class="header">
        Our
        <span class="header_services">services</span>
      </div>
      <div class="services__blocks">
        <el-row>
          <el-col
            v-for="(block, index) of blocks"
            :key="index"
            :xs="12"
            :sm="8"
            :md="6"
            class="services_block__container"
          >
            <div class="services_block">
              <div class="img" :style="{ backgroundImage: 'url(' + block.background + ')' }">
                <img :class="block.class" :src="block.src">
              </div>
              <div class="description">
                {{ block.description }}
              </div>
            </div>
          </el-col>
        </el-row>
      </div>
      <div class="services_description">
        Based on our previous expertise in Web/Mobile development, experience with a Product solutions and Design, we are always doing our best to provide you with the expected results.
      </div>
      <nuxt-link tag="button" to="/our-services" class="services__button">
        More details
      </nuxt-link>
    </div>
  </section>
</template>
<script>
export default {
  data () {
    return {
      blocks: [
        { description: 'Web development', class: 'web', src: require('../../assets/main/services/123/settings.gif'), background: require('../../assets/main/services/123/web.png') },
        { description: 'Mobile development', class: 'mob', src: require('../../assets/main/services/123/settings.gif'), background: require('../../assets/main/services/123/mob.png') },
        { description: 'UI/UX design', class: 'design', src: require('../../assets/main/services/123/pen.gif'), background: require('../../assets/main/services/123/web.png') },
        { description: 'Legacy Code Redevelopment', class: 'legacy', src: require('../../assets/main/services/123/synbol.gif'), background: require('../../assets/main/services/123/legacy.png') },
        { description: 'Consulting/Estimation', class: 'message', src: require('../../assets/main/services/123/message2.gif'), background: require('../../assets/main/services/123/message.png') },
        { description: 'Code Review', class: 'review', src: require('../../assets/main/services/123/magnifier.gif'), background: require('../../assets/main/services/123/web.png') },
        { description: 'Software Maintenance', class: 'maintence', src: require('../../assets/main/services/123/wrench.gif'), background: require('../../assets/main/services/123/web.png') },
        { description: 'Product development and support', class: 'support', src: require('../../assets/main/services/123/support2.gif'), background: require('../../assets/main/services/123/support.png') }
      ]
    }
  }
}
</script>
<style scoped>
  .our__services{
    width: 100%;
    padding: 100px 0;
    display: flex;
    justify-content: center;
    align-items: center;
  }
  .our__services__container{
    padding: 10px;
    display: flex;
    flex-direction: column;
    justify-content: flex-start;
    align-items: center;
    width: 1100px;
    height: 100%;
  }
  .header{
    font-weight: 400;
    font-size: 35px;
    color: #fff;
  }
  .header_services{
    color: #228A43;
    border-bottom: 1px solid #228A43;
  }
  .services__blocks{
    width: 100%;
    margin-top: 50px;
  }
  .img{
    background-size: contain;
    background-repeat: no-repeat;
    background-position: center;
    width: 140px;
    height: 100px;
    display: flex;
    justify-content: center;
    align-items: center;
  }
  .web {
    width: 50%;
    height: 60%;
    margin-bottom: 15px;
  }
  .mob{
    margin: 0 0 10px 64px;
    width: 22%;
    height: 26%;
  }
  .design{
    width: 60%;
    height: 60%;
    margin-bottom:15px;
  }
  .legacy{
    width: 30%;
    height: 50%;
    margin: 0 0 24px 65px;
  }
  .message{
    width: 60%;
    height: 30%;
    margin: 0 0 23px 0;
  }
  .review{
    width: 80%;
    height: 70%;
    margin-bottom:15px;
  }
  .maintence{
    width: 90%;
    height: 75%;
    margin-bottom:15px;
  }
  .support{
    width: 40%;
    height: 40%;
    margin: 0 44px 10px 0;
  }
  .services_block__container{
    display: flex;
    justify-content: center;
    align-items: center;
  }
  .services_block{
    margin-top: 25px;
    box-sizing: border-box;
    width: 180px;
    min-height: 155px;
    display: flex;
    flex-direction: column;
    justify-content: flex-start;
    align-items: center;
  }
  .description{
    margin-top: 25px;
    color: #fff;
    text-align: center;
    font-size: 18px;
  }
  .services_description{
    max-width: 920px;
    text-align: center;
    font-weight: 300;
    font-size: 23px;
    line-height: 31px;
    margin-top: 50px;
    color: #A5A5A5;
  }
  .services__button{
    margin-top: 80px;
    width: 220px;
    height: 50px;
    background: rgba(255, 255, 255, 0.01);
    border: 1px solid #228A43;
    backdrop-filter: blur(10px);
    border-radius: 5px;
    color: #fff;
    font-size: 18px;
    transition: all 0.3s;
    font-weight: bold;
    cursor: pointer;
  }
  .services__button:hover{
    background-color: #228A43;
  }
  @media screen and (max-width: 440px) {
    .description{
      font-size: 14px;
    }
  }
</style>
