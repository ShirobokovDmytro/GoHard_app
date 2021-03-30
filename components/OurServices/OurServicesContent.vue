<template>
  <section class="our_services__content">
    <div class="our_services__content__container">
      <p class="our_services__description">
        We are a fast-growing software development agency with a strong expertise in the most relevant and innovative programming languages, frameworks, libraries and tools. We
        are a fast-growing software development agency with a strong expertise in the
        most relevant and innovative programming languages, frameworks,
        libraries and tools.
      </p>
      <div class="our_services__blocks">
        <div v-for="(block, index) of blocks" :key="index" class="block" :class="block.position">
          <div class="caption">
            <div class="caption__number">
              <div class="img" :style="{ backgroundImage: 'url(' + block.background + ')' }">
                <img :class="block.class" :src="block.src">
              </div>
            </div>
            <div class="caption__description">
              <div class="heading-green">
                {{ block.heading_1 }}
              </div>
              {{ block.heading_2 }}
            </div>
          </div>
          <div class="description">
            {{ block.description }}
          </div>
        </div>
      </div>
    </div>
  </section>
</template>
<script>
export default {
  data () {
    return {
      blocks: [
        { class: 'web', position: 'left', src: require('../../assets/main/services/123/settings.png'), background: require('../../assets/main/services/123/web.png'), heading_1: 'Web', heading_2: 'Development', description: 'We are always ready to discuss your request and find the best solutions for your case. Also, one of our developers could be a part of your team on one of the existing projects as an outstaff member.' },
        { class: 'mob', position: 'right', src: require('../../assets/main/services/123/settings.png'), background: require('../../assets/main/services/123/mob.png'), heading_1: 'Mobile', heading_2: 'Development', description: 'Our stack covers Android Native, iOS Native and Cross-platform development. Depending on your idea, business objectives and requirements we will estimate, discover and implement the project in the most relevant way to provide each case with the expected quality and result.' },
        { class: 'design', position: 'left', src: require('../../assets/main/services/123/pen.png'), background: require('../../assets/main/services/123/design_bg.png'), heading_1: 'UI/UX', heading_2: 'Design', description: 'Our experienced and creative designers are always looking for a possibility to use their inspiration to achieve the desired result, why not on your project?' },
        { class: 'legacy ', position: 'right', src: require('../../assets/main/services/123/synbol.png'), background: require('../../assets/main/services/123/legacy.png'), heading_1: 'Legacy Code', heading_2: 'Redevelopment', description: 'Have an existing project and would like to update it? Would be great to find the best solution for you, according to the most innovative technologies and tools.' },
        { class: 'message ', position: 'left', src: require('../../assets/main/services/123/message2.gif'), background: require('../../assets/main/services/123/message.png'), heading_1: 'Consulting', heading_2: 'Estimation', description: 'Have a project and a team of developers? We could estimate and consult about the best technologies stack. In order to make you be sure you are provided with the best possible solution.' },
        { class: 'review ', position: 'right', src: require('../../assets/main/services/123/magnifier.png'), background: require('../../assets/main/services/123/rewiew.png'), heading_1: 'Code', heading_2: 'Review', description: 'Have a project and a team of developers? We could estimate and consult about the best technologies stack. In order to make you be sure you are provided with the best possible solution.' },
        { class: 'maintence ', position: 'left', src: require('../../assets/main/services/123/support.gif'), background: require('../../assets/main/services/123/web.png'), heading_1: 'Software', heading_2: 'Maintenance', description: 'We are always ready to support and advise your project after the development process is finished.' },
        { class: 'support ', position: 'right', src: require('../../assets/main/services/123/support2.png'), background: require('../../assets/main/services/123/support.png'), heading_1: 'Product', heading_2: 'Development', description: 'Previous experience in creating an idea, development and support of different solutions in the Medical and Telecommunication fields gives us a quite deep understanding of business processes and the ways of solving issues. That’s why our product managers can provide you with some advice for further improvements.' }
      ]
    }
  }
}
</script>
<style scoped>
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
.our_services__content{
  width: 100%;
  height: 100%;
  display: flex;
  justify-content: center;
  align-items: center;
}
.our_services__content__container{
  width: 1100px;
  padding: 50px 25px;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
}
.our_services__description{
  text-align: center;
  font-size: 23px;
  color: #A5A5A5;
  max-width: 750px;
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
.our_services__blocks{
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: flex-start;
}
.our_services__blocks:first-child{
  background-color: red;
}
.block{
  border-radius: 5px;
  padding: 15px;
  width: 750px;
  min-height: 250px;
  border: 1px solid #a5a5a5;
  backdrop-filter: blur(26px);
  display: flex;
  box-shadow: 0 0 8px rgba(34, 138, 67, 0.35);
}
.caption{
  padding: 5px;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  flex-wrap: wrap;
  width: 350px;
  height: auto;
  color: #228A43;
  box-sizing: border-box;
}
.caption__number{
  height: auto;
  font-size: 96px;
  text-align: center;
  margin-bottom: -30px;
}
.heading-green{
  color: #228A43;
}
.caption__description{
  text-align: center;
  font-size: 24px;
  font-weight: 700;
  color: #fff;
  margin-top: 40px;
}
.description{
  width: 100%;
  color: #A5A5A5;
  font-size: 18px;
  text-align: center;
  display: flex;
  justify-content: center;
  align-items: center;
}
.left {
  margin: 25px 300px 25px 0;
}
.right{
  margin: 25px 0 25px 300px;
}

@media screen and (max-width: 1100px){
  .caption{
    width: 100%;
  }
  .our_services__content__container{
    width: 100%;
    padding: 25px;
  }
  .block{
    margin: 25px 0;
  }
}
@media screen and (max-width: 800px){
  .caption{
    width: 100%;
  }
  .block{
    width: 100%;
    height: auto;
  }
}
@media screen and (max-width: 620px){
  .block{
    flex-direction: column;
    height: auto;
  }
  .description{
    width: auto;
  }
}
</style>
