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
      <p class="services_description">
        Based on our previous expertise in Web/Mobile development, experience with a Product solutions and Design, we are always doing our best to provide you with the expected results.
      </p>
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
        { description: 'Web development', class: 'web', src: require('../../assets/main/services/123/settings.png'), background: require('../../assets/main/services/123/web.png') },
        { description: 'Mobile development', class: 'mob', src: require('../../assets/main/services/123/settings.png'), background: require('../../assets/main/services/123/mob.png') },
        { description: 'UI/UX design', class: 'design', src: require('../../assets/main/services/123/pen.png'), background: require('../../assets/main/services/123/design_bg.png') },
        { description: 'Legacy Code Redevelopment', class: 'legacy', src: require('../../assets/main/services/123/synbol.png'), background: require('../../assets/main/services/123/legacy.png') },
        { description: 'Consulting/Estimation', class: 'message', src: require('../../assets/main/services/123/message2.gif'), background: require('../../assets/main/services/123/message.png') },
        { description: 'Code Review', class: 'review', src: require('../../assets/main/services/123/magnifier.png'), background: require('../../assets/main/services/123/rewiew.png') },
        { description: 'Software Maintenance', class: 'maintence', src: require('../../assets/main/services/123/support.gif'), background: require('../../assets/main/services/123/web.png') },
        { description: 'Product development and support', class: 'support', src: require('../../assets/main/services/123/support2.png'), background: require('../../assets/main/services/123/support.png') }
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
    width: 60px;
    height: 60px;
    margin-bottom: 15px;
    -webkit-animation:spin 4s linear infinite;
    -moz-animation:spin 4s linear infinite;
    animation:spin 4s linear infinite;
  }
  @-moz-keyframes spin { 100% { -moz-transform: rotate(360deg); } }
  @-webkit-keyframes spin { 100% { -webkit-transform: rotate(360deg); } }
  @keyframes spin { 100% { -webkit-transform: rotate(360deg); transform:rotate(360deg); } }
  .mob{
    margin: 0 0 10px 64px;
    width: 25px;
    height: 25px;
    -webkit-animation:spin 4s linear infinite;
    -moz-animation:spin 4s linear infinite;
    animation:spin 4s linear infinite;
  }
  .design{
    width: 30px;
    height: 30px;
    margin-bottom:45px;
    animation:move 2.5s ease-in-out infinite;
  }
  @keyframes move {
    0% {
      margin-bottom:45px;
    }
    25% {
      margin: 10px -65px 0 0;
    }
    50% {
      margin: 35px 40px 0 0;
    }
    100%{
      margin-bottom:45px;
    }
  }
  .legacy{
    width: 11px;
    height: 40px;
    margin: 0 0 28px 68px;
    animation: fadeInFromNone 1.5s ease-in infinite;
  }
  @keyframes fadeInFromNone {
    0% {
      opacity: 1;
    }
    100% {
      opacity: 0.2;
    }
  }
  .message{
    width: 40%;
    height: 20%;
    margin: 0 0 25px 0;
  }
  .review{
    width: 30px;
    height: 30px;
    margin-bottom:50px;
    animation:review 2.5s ease-in-out infinite;
  }
  @keyframes review {
    0% {
      margin: 0 0 0 50px;
    }
    25% {
      margin: 0 0 50px 0;
    }
    50% {
      margin: 0 55px 0 0;
    }
    75%{
      margin: 20px 0 0 0;
    }
    100% {
      margin: 0 0 0 50px;
    }
  }
  .maintence{
    width: 110px;
    height: 65px;
    margin-bottom:15px;
  }
  .support{
    width: 40px;
    height: 40px;
    margin: 0 0 10px 75px;
    animation: fadeInFromNone 1.5s ease-in infinite;
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
