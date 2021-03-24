<template>
  <div class="technologies__content">
    <div class="technologies__container">
      <div v-for="(block, index) of blocks" :key="index">
        <div class="slider__container">
          <div class="slider__heading">
            <span class="head_1">{{ block.head_1 }}</span> {{ block.head_2 }}
          </div>
          <div class="slider__description">
            {{ block.description }}
          </div>
          <el-carousel :interval="2000" indicator-position="none" height="400px" type="card">
            <el-carousel-item v-for="(item, item_index) in block.slides" :key="item_index">
              <img class="carousel--img" :src="item.img" alt="js">
              <div class="carousel--heading">
                {{ item.head }}
              </div>
              <div class="carousel--description">
                {{ item.description }}
              </div>
            </el-carousel-item>
          </el-carousel>
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
          head_1: 'Front-end',
          head_2: 'development',
          description: 'Front-end is the brightest showcase how your website can look and felt by users. User friendly design and functionality makes the difference in the way how users perceive the information.',
          slides: [
            {
              img: require('../../assets/technologies/Front/js.png'),
              head: 'JS',
              description: 'JavaScript is a lightweight, interpreted, or just-in-time compiled programming language with first-class functions.'
            },
            {
              img: require('../../assets/technologies/Front/react.png'),
              head: 'React.js',
              description: 'React can be used to develop single page and mobile apps. Its goal is to provide high speed, simplicity and scalability. As a library for developing user interfaces, React is often used with other libraries such as MobX, Redux, and GraphQL.'
            },
            {
              img: require('../../assets/technologies/Front/vue.png'),
              head: 'Vue.js',
              description: 'Vue is a progressive framework for building user interfaces. Unlike other monolithic frameworks, Vue is designed from the ground up to be incrementally adoptable.'
            },
            {
              img: require('../../assets/technologies/Front/html.png'),
              head: 'HTML',
              description: 'HTML is the standard markup language for Web pages.'
            },
            {
              img: require('../../assets/technologies/Front/css.png'),
              head: 'CSS',
              description: 'CSS describes how HTML elements are to be displayed.'
            },
            {
              img: require('../../assets/technologies/Front/bootstrap.png'),
              head: 'Bootstrap',
              description: 'Quickly design and customize responsive mobile-first sites with Bootstrap.'
            },
            {
              img: require('../../assets/technologies/Front/material.png'),
              head: 'Material-UI',
              description: 'React component for faster and easier web development.'
            },
            {
              img: require('../../assets/technologies/Front/elements.png'),
              head: 'Element',
              description: 'Element, a Vue 2.0 based component library for developers, designers and product managers'
            },
            {
              img: require('../../assets/technologies/Front/nuxt.png'),
              head: 'Nuxt.js',
              description: 'An open source framework making web development simple and powerful.'
            },
            {
              img: require('../../assets/technologies/Front/next.png'),
              head: 'Next.js',
              description: 'Next.js gives you the best developer experience with all the features you need for production: hybrid static & server rendering.'
            }
          ]
        },
        {
          head_1: 'Back-end',
          head_2: 'development',
          description: 'Quality of back-end on your project is a direct characteristic of the quality of the project. That is why the right choice of technologies used, is so important.',
          slides: [
            {
              img: require('../../assets/technologies/back/node.png'),
              head: 'Node.js',
              description: 'Node.js is an open-source, cross-platform, back-end JavaScript runtime environment that runs on the V8 engine and executes JavaScript code outside a web browser.'
            },
            {
              img: require('../../assets/technologies/back/express.png'),
              head: 'Express.js',
              description: 'Express.js is a back end web application framework for Node.js, released as free and open-source software under the MIT License.'
            },
            {
              img: require('../../assets/technologies/back/php.png'),
              head: 'PHP',
              description: 'PHP is a general-purpose scripting language especially suited to web development. The PHP reference implementation is now produced by The PHP Group.'
            },
            {
              img: require('../../assets/technologies/back/laravel.png'),
              head: 'Laravel',
              description: 'Laravel is a free, open-source PHP web framework, created by Taylor Otwell and intended for the development of web applications following the model–view–controller (MVC) architectural pattern and based on Symfony.'
            },
            {
              img: require('../../assets/technologies/back/syphony.png'),
              head: 'Symfony',
              description: 'Symfony is a PHP web application framework and a set of reusable PHP components/libraries. It was published as free software on October 18, 2005 and released under the MIT license.'
            },
            {
              img: require('../../assets/technologies/back/pytone.png'),
              head: 'Python',
              description: 'Python is an interpreted, high-level and general-purpose programming language. Python\'s design philosophy emphasizes code readability with its notable use of significant indentation.'
            },
            {
              img: require('../../assets/technologies/back/django.png'),
              head: 'Django',
              description: 'Django is a Python-based free and open-source web framework that follows the model-template-views (MTV) architectural pattern.'
            },
            {
              img: require('../../assets/technologies/back/flack.png'),
              head: 'Flask',
              description: 'Flask is a micro web framework written in Python. It is classified as a microframework because it does not require particular tools or libraries.'
            },
            {
              img: require('../../assets/technologies/back/golang.png'),
              head: 'Golang',
              description: 'Go is a statically typed, compiled programming language designed at Google by Robert Griesemer, Rob Pike, and Ken Thompson.'
            },
            {
              img: require('../../assets/technologies/back/begoo.png'),
              head: 'Beego',
              description: 'Beego is a RESTful HTTP framework for the rapid development of Go applications including APIs, web apps and backend services with integrated Go specific features such as interfaces and struct embedding.'
            },
            {
              img: require('../../assets/technologies/back/sql.png'),
              head: 'MySQL',
              description: 'MySQL is an open-source relational database management system (RDBMS). A relational database organizes data into one or more data tables in which data types may be related to each other;'
            },
            {
              img: require('../../assets/technologies/back/postgresql.png'),
              head: 'PostgreSQL',
              description: 'PostgreSQL also known as Postgres, is a free and open-source relational database management system (RDBMS) emphasizing extensibility and SQL compliance.'
            },
            {
              img: require('../../assets/technologies/back/mongodb.png'),
              head: 'MongoDB',
              description: 'MongoDB is a source-available cross-platform document-oriented database program. Classified as a NoSQL database program, MongoDB uses JSON-like documents with optional schemas.'
            }
          ]
        },
        {
          head_1: 'Mobile',
          head_2: 'development',
          description: 'Depending on the requirements, business idea and final expectations, we can choose technologies and implement requests in the most reasonable way.',
          slides: [
            {
              img: require('../../assets/technologies/mobile/objective_C.png'),
              head: 'Objective-C',
              description: 'Objective-C is a general-purpose, object-oriented programming language that adds Smalltalk-style messaging to the C programming language. It was the main programming language supported by Apple'
            },
            {
              img: require('../../assets/technologies/mobile/cross_flutter.png'),
              head: 'Flutter',
              description: 'Flutter is an open-source UI software development kit created by Google. It is used to develop applications for Android, iOS, Linux, Mac, Windows, Google Fuchsia, and the web from a single codebase.'
            },
            {
              img: require('../../assets/technologies/mobile/java.png'),
              head: 'Java',
              description: 'Java is a class-based, object-oriented programming language that is designed to have as few implementation dependencies as possible.'
            },
            {
              img: require('../../assets/technologies/mobile/kotlin.png'),
              head: 'Kotlin',
              description: 'Kotlin is a cross-platform, statically typed, general-purpose programming language with type inference. Kotlin is designed to interoperate fully with Java, and the JVM version of Kotlin\'s standard library depends on the Java Class Library, but type inference allows its syntax to be more concise.'
            },
            {
              img: require('../../assets/technologies/mobile/react.png'),
              head: 'React Native',
              description: 'React Native is an open-source mobile application framework. It is used to develop applications for Android, Android TV, iOS, macOS, tvOS, Web, Windows and UWP by enabling developers to use React\'s framework along with native platform capabilities.'
            },
            {
              img: require('../../assets/technologies/mobile/swift.png'),
              head: 'Swift',
              description: 'Swift is a general-purpose, multi-paradigm, compiled programming language developed by Apple Inc. and the open-source community, first released in 2014.'
            }
          ]
        }
      ]
    }
  }
}
</script>
<style scoped>
.heading{
  color: #228A43;
  font-size: 50px;
  font-weight: bold;
}
.el-carousel__item h3 {
  color: #475669;
  font-size: 14px;
  opacity: 0.75;
  line-height: 200px;
  margin: 0;
}
.el-carousel--horizontal{
  margin-top: 50px;
  padding-top: 20px;
  width: auto;
  height: 450px;
  overflow-y: hidden;
}
.el-carousel__item:nth-child(2n) {
  margin-top: 15px;
  background-color: black;
  border-radius: 11px;
  display: flex;
  justify-content: center;
  align-items: center;
  flex-direction: column;
}
.el-carousel__item:nth-child(2n+1) {
  margin-top: 15px;
  background-color: black;
  border-radius: 11px;
  display: flex;
  justify-content: center;
  align-items: center;
  flex-direction: column;
}

.el-carousel__item--card.is-active {
  box-shadow: 0 0 44px rgba(255, 255, 255, 0.25);
}
.technologies__content{
  width: 100%;
  height: 100%;
  display: flex;
  justify-content: center;
  align-items: center;
}
.technologies__container{
  width: 1100px;
  padding: 50px 25px;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
}
.slider__heading{
  text-align: center;
  font-size: 35px;
  color: #FFFFFF;
  font-weight: 700;
  margin: 80px 0 40px 0;
}
.head_1{
  color: #228A43;
}
.technologies__description, .slider__description{
  text-align: center;
  font-size: 23px;
  color: #A5A5A5;
  max-width: 750px;
}
.carousel--img{
  width: 110px;
  height: auto;
}
.carousel--heading{
  font-size: 35px;
  color: #FFFFFF;
  margin: 20px 0;
}
.carousel--description{
  text-align: center;
  font-weight: 300;
  font-size: 17px;
  color: #a5a5a5;
  margin: 0 15px;
}
@media screen and (max-width: 450px){
  .carousel--heading{
    font-size: 18px;
  }
  .carousel--img{
    width: 60%;
    height: auto;
  }
  .carousel--description{
    font-size: 12px;
  }
}
</style>
<style>
.el-carousel__mask{
  background-color: black!important;
}
</style>
