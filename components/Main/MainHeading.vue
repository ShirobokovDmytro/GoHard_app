<template>
  <section class="main__container">
    <h1>
      Software <br>
      <span>development</span>
      services
    </h1>
  </section>
</template>
<style scoped>
  .main__container{
    width: 100%;
    min-height: 100vh;
    background-image: url(@/assets/main/bg_main.png);
    background-repeat: no-repeat;
    background-position: center;
    background-size: contain;
    display: flex;
    justify-content: center;
    align-items: center;
  }
  h1{
    margin-left: -3px;
    color: #fff;
    font-size: 100px;
    line-height: 86px;
  }

  @media screen and (max-width: 1100px){
    .main__container{
      width: 100%;
      background-image: url(@/assets/main/bg_main.png);
      display: flex;
      justify-content: center;
      align-items: center;
    }
    h1{
      margin-top: 120px;
      font-size: 8vw;
    }
  }
  @media screen and (min-width: 600px){
    span{
      color: #FFF;
      background-clip: text;
      -webkit-text-fill-color: transparent;
      -webkit-text-stroke: 2px #228A43;
    }
  }
  @media screen and (max-width: 600px){
    h1{
      line-height: 40px;
    }
    span{
      color: #228A43;
    }
  }
  @media screen and (orientation:landscape) {
    .main__container{
      margin-top: 60px;
    }
  }
</style>
