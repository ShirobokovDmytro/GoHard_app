<template>
  <section class="main__portfolio">
    <div class="main__portfolio__container">
      <h3 class="header">
        Portfolio
      </h3>
      <p class="portfolio__description">
        Here are some of our previous projects that we worked on and implemented customers requirements and ideas,
        in order to achieve their business objectives.
      </p>
      <nuxt-link tag="button" to="/portfolio" class="our__works__button">
        Our works
      </nuxt-link>
    </div>
  </section>
</template>
<style scoped>
  .main__portfolio{
    width: 100%;
    display: flex;
    justify-content: center;
    align-items: center;
  }
  .main__portfolio__container{
    display: flex;
    flex-direction: column;
    justify-content: flex-start;
    align-items: center;
    width: 1100px;
    height: 100%;
    padding: 100px 0;
  }
  .header{
    font-weight: 400;
    font-size: 35px;
    color: #228A43;
    border-bottom: 1px solid #228A43;
  }
  .portfolio__description{
    margin-top: 30px;
    font-weight: 300;
    font-size: 23px;
    text-align: center;
    line-height: 31px;
    color: #A5A5A5;
  }
  .our__works__button{
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
  .our__works__button:hover{
    background-color: #228A43;
  }
  @media screen and (max-width: 1100px){
    .main__portfolio__container{
      padding: 25px;
      width: 100%;
    }
  }
</style>
