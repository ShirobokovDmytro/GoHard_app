<template>
  <div class="portfolio_content">
    <div class="portfolio_container">
      <h2 class="heading">
        Our works
      </h2>
      <div class="portfoio_description">
        Here are some of our most relevant and challenging projects that we worked with and implemented customers requirements and ideas, in order to achieve their business objectives.
      </div>
      <div class="portfolio__blocks">
        <div v-for="(block, index) of blocks" :key="index" class="block">
          <img class="block_image" :src="block.background" alt="image" :class="block.class">
          <div class="block_content">
            <div class="content_heading">
              {{ block.heading }}
            </div>
            <div class="content_description">
              {{ block.description }}
            </div>
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
        {
          heading: 'Website for delivering cars from USA',
          description: 'The website for cars delivery services from USA to Eastern Europe.\n' +
            'This client wanted to enlarge his business in order to find new display and ways to provide his services.\n' +
            'We have implemented his request to build a reliable platform to make this fast and convenient.\n' +
            'The stack was connected Vue.js, Vuetify, SCSS.',
          background: require('../../assets/portfolio/works/2.png'),
          class: 'left'
        },
        {
          heading: 'Medical equipment website',
          description: 'The task was to create working website for current company with all of their equipment and warehouses. The client was fully satisfied.\n' +
            '(html, css, JQuery, Javascript)\n' +
            '\n' +
            'Onco.net\n' +
            'Website for Ukraine’s first oncological screening center! (JavaScript, PHP, HTML, CSS)',
          background: require('../../assets/portfolio/works/4.png'),
          class: 'right'
        },
        {
          heading: 'Medical equipment website',
          description: `This is the company with 100% of foreign investments. It is situated in USA. It has the warehouses with medical imaging equipment and the spare parts, capacities and resources for repair and service of the medical imaging equipment of world known brands.
                        The task was to create working website for current company with all of their equipment and warehouses. We should provide clear description and some support in future.
                        I had done this job totally well, so the client was fully satisfied.
                        ((html, css, JQuery, Javascript))less
                        Show less text
                        http://lee-im.com`,
          background: require('../../assets/portfolio/works/5.jpg'),
          class: 'left'
        },
        {
          heading: 'Medical equipment website',
          description: `This is the company with 100% of foreign investments. It is situated in USA. It has the warehouses with medical imaging equipment and the spare parts, capacities and resources for repair and service of the medical imaging equipment of world known brands.
                        The task was to create working website for current company with all of their equipment and warehouses. We should provide clear description and some support in future.
                        I had done this job totally well, so the client was fully satisfied.
                        ((html, css, JQuery, Javascript))less
                        Show less text
                        http://lee-im.com`,
          background: require('../../assets/portfolio/works/1.png'),
          class: 'right'
        },
        {
          heading: 'Medical equipment website',
          description: `This is the company with 100% of foreign investments. It is situated in USA. It has the warehouses with medical imaging equipment and the spare parts, capacities and resources for repair and service of the medical imaging equipment of world known brands.
                        The task was to create working website for current company with all of their equipment and warehouses. We should provide clear description and some support in future.
                        I had done this job totally well, so the client was fully satisfied.
                        ((html, css, JQuery, Javascript))less
                        Show less text
                        http://lee-im.com`,
          background: require('../../assets/portfolio/works/3.png'),
          class: 'left'
        }
      ]
    }
  }
}
</script>
<style>
.portfolio_content{
  width: 100%;
  height: 100%;
  display: flex;
  justify-content: center;
  align-items: center;
}
.portfolio_container{
  width: 1100px;
  padding: 50px 25px;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
}
.heading{
  color: #228A43;
  font-size: 50px;
  font-weight: bold;
}
.portfoio_description{
  text-align: center;
  font-size: 23px;
  color: #A5A5A5;
  max-width: 850px;
  margin-bottom: 25px;
}
.portfolio__blocks{
  width: 100%;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
}
.block{
  margin-top: 25px;
  width: 100%;
  min-height: 250px;
  border: 1px solid #606060;
  box-sizing: border-box;
  border-radius: 5px;
}
.block_image{
  width: 40%;
  height: 250px;
}
.left{
  float: left;
  border-radius: 5px 0 0 5px;
}
.right{
  float: right;
  border-radius: 0 5px 5px 0;
}
.block_content{
  width: auto;
  min-height: 250px;
  display: flex;
  flex-direction: column;
  justify-content: flex-start;
  align-items: flex-start;
}
.content_heading{
  font-size: 25px;
  color: #FFFFFF;
  font-weight: 400;
  padding: 15px;
}
.content_description{
  padding: 15px;
  color: #a5a5a5;
  font-size: 15px;
  line-height: 22px;
}

@media screen and (max-width: 1100px){
  .portfolio_container{
    width: 100%;
    padding: 25px;
  }
}
@media screen and (max-width: 1040px){
  .block{
    max-width: 500px;
    display: flex;
    flex-direction: column;
  }
  .block_image{
    width: 100%;
    height: auto;
    border-radius: 5px 5px 0 0;
  }
}
@media screen and (max-width: 700px){
  .portfoio_description{
    width: auto;
  }
}
</style>
