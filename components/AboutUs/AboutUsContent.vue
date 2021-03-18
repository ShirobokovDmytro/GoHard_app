<template>
  <div class="about_us__content">
    <div class="about_us__content__container">
      <p class="about_us__description">
        We are a fast-growing software development agency with a strong expertise
        in the most relevant and innovative programming languages,
        frameworks, libraries and tools. We are a fast-growing
        software development agency with a strong
        expertise in the most relevant and innovative
        programming languages, frameworks,
        libraries and tools.
      </p>
      <div class="about_us__blocks">
        <div class="block" v-for="(block, index) of blocks" :key="index" :class="block.class">
          <div class="caption">
            <div class="caption__number">
              {{block.number}}
            </div>
            <div class="caption__description">
              {{block.heading}}
            </div>
          </div>
          <div class="description">
            {{block.description}}
          </div>
        </div>
      </div>
    </div>
  </div>
</template>
<script>
export default {
  data () {
    return {
      blocks: [
        { class: 'left', number: 5, heading: 'Most relevant and innovative programming languages', description: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit. Dui eget sit vel dolor mauris. Aliquet mauris pellentesque euismod sagittis, condimentum nec.Lorem ipsum dolor sit amet, consectetur adipiscing elit. Dui eget sit vel dolor mauris. Aliquet mauris pellentesque euismod sagittis, condimentum nec.' },
        { class: 'right', number: 4, heading: 'Fields of business we implement solutions for', description: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit. Dui eget sit vel dolor mauris. Aliquet mauris pellentesque euismod sagittis, condimentum nec.Lorem ipsum dolor sit amet, consectetur adipiscing elit. Dui eget sit vel dolor mauris. Aliquet mauris pellentesque euismod sagittis, condimentum nec.' },
        { class: 'left', number: 2, heading: 'Years of work at the market', description: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit. Dui eget sit vel dolor mauris. Aliquet mauris pellentesque euismod sagittis, condimentum nec.Lorem ipsum dolor sit amet, consectetur adipiscing elit. Dui eget sit vel dolor mauris. Aliquet mauris pellentesque euismod sagittis, condimentum nec.' },
        { class: 'right', number: 1, heading: 'United teamof professionals', description: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit. Dui eget sit vel dolor mauris. Aliquet mauris pellentesque euismod sagittis, condimentum nec.Lorem ipsum dolor sit amet, consectetur adipiscing elit. Dui eget sit vel dolor mauris. Aliquet mauris pellentesque euismod sagittis, condimentum nec.' }
      ]
    }
  }
}
</script>
<style scoped>
  .about_us__content{
    width: 100%;
    height: 100%;
    display: flex;
    justify-content: center;
    align-items: center;
  }
  .about_us__content__container{
    width: 1100px;
    padding: 50px 25px;
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
  }
  .about_us__description{
    text-align: center;
    font-size: 23px;
    color: #A5A5A5;
    max-width: 750px;
  }
  .about_us__blocks{
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: flex-start;
  }
  .block{
    border-radius: 5px;
    width: 750px;
    height: 250px;
    border: 1px solid #a5a5a5;
    backdrop-filter: blur(26px);
    display: flex;
    box-shadow: 0px 0px 44px rgba(34, 138, 67, 0.35);
  }
  .caption{
    padding: 5px;
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    flex-wrap: wrap;
    width: 350px;
    height: 100%;
    color: #228A43;
    box-sizing: border-box;
  }
  .caption__number{
    font-size: 96px;
    line-height: 130px;
    text-align: center;
  }
  .caption__description{
    text-align: center;
    font-size: 18px;
    color: #fff;
  }
  .description{
    padding: 25px;
    width: 100%;
    color: #A5A5A5;
    font-size: 18px;
    text-align: center;
    display: flex;
    justify-content: center;
    align-items: center;
  }
  .left{
    margin: 25px 300px 25px 0;
  }
  .right{
    margin: 25px 0 25px 300px;
  }
  @media screen and (max-width: 1100px){
    .about_us__content__container{
      width: 100%;
      padding: 25px;
    }
    .block{
      margin: 25px 0;
    }
  }
  @media screen and (max-width: 800px){
    .block{
      width: 100%;
      height: auto;
    }
  }
  @media screen and (max-width: 560px){
    .block{
      flex-direction: column;
      height: auto;
    }
    .caption{
      width: 100%;
    }
    .description{
      width: auto;
    }
  }
</style>
