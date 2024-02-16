
<template>
    <div class="resume" id="resume">
      <div class="container">
        <section>
          <h2>Education</h2>
          <div class="card cardd" v-for="content in educationContent" :key="content.year"  data-aos="fade-up">
            <h4>{{ content.year }}</h4>
            <div class="card-body">
              <p>{{ content.description }}</p>
            </div>
          </div>
        </section>
  
        <section >
          <h2 class="skill-top">Skills</h2>
          <div class="row">
            <div class="col-md-4 mx-auto scard" v-for="content in skillContent" :key="content.title" >
              <div class="card mb-3 skillcard" data-aos="flip-down">
                <span></span>
                <span></span>
                <span></span>
                <span></span>
                <img :src="content.picture" class="card-img-top" alt="{{ content.title }}">
                <div class="card-body">
                  <h3 class="card-title">{{ content.title }}</h3>
                </div>
              </div>
            </div>
          </div>
        </section>
      </div>
    </div>
  </template>
  
  <script>
  export default {
    data() {
      return {
        educationContent: [
          {
            year: "2023",
            description: "Studied coding at Life Choice Academy for 6 months",
          },
          {
            year: "2020-2022",
            description: "Attended Cape Peninsula University of Technology to study Biotechnology; didn't complete my degree"
          },
          {
            year: "2015-2019",
            description: "Matriculated at Spine Road High School with a bachelor pass"
          }
        ],
        skillContent: [
          {
            picture: "https://i.ibb.co/mhjXc48/icons8-html-480.png",
            title: "HTML5"
          },
          {
            picture: "https://i.ibb.co/0hT4N41/icons8-css-480.png",
            title: "CSS3"
          },
          {
            picture: "https://i.ibb.co/wpc2V5N/icons8-bootstrap-480.png",
            title: "Bootstrap"
          },
          {
            picture: "https://i.ibb.co/sJy7W6J/icons8-javascript-480.png",
            title: "JavaScript"
          },
          {
            picture: "https://i.ibb.co/nR9jFbn/icons8-mysql-480.png",
            title: "Vue.js"
          },
          {
            picture: "https://i.ibb.co/ZTHTmPg/icons8-vue-js-480.png",
            title: "MySQL"
          }
        ]
      };
    }
  };
  </script>
  
  <style scoped>
    section {
      margin-bottom: 2em;
    }
  
    .cardd {
      margin: 50px 0;
      border-radius: 20px;
      padding: 2px;
      width: 50%;
      border: 2px solid black;
      background: rgb(71, 70, 67);
    }
    .cardd p{
      color: white;
    }
  
  .cardd:nth-child(odd) {
      box-shadow: 0.5vw 0.2vw 0.7vw rgba(133,29,170,255);
    }
  
    .cardd:nth-child(even) {
      box-shadow: -0.5vw 0.2vw 0.7vw rgba(133,29,170,255);
      margin-left: auto;
    }
  
    @media screen and (max-width: 900px) {
      .cardd {
        width: 100%;
        flex-wrap: wrap;
      }
  
      .cardd p{
        font-size: small;
      }
  
      .cardd:nth-child(odd),
      .cardd:nth-child(even) {
        margin-left: 0;
    
      }
  
      .cardd:nth-child(odd)::after,
      .cardd:nth-child(even)::after {
        content: none;
      }
    }
    .resume{
      padding-top: 5rem;
    }
    h2{
      padding-bottom: 2rem;
    }
    .skill-top{
      padding-top: 2rem;
    }

    .skillcard{
      background:rgb(71, 70, 67);
      position: relative;
      box-shadow: 0 10px 10px rgb(232, 58, 214, 0.3);
      overflow:hidden
    }
    .skillcard span{
      transition: 0.5;
      opacity: 0;
    }
    .skillcard:hover span{
      opacity: 100;
    }
    .skillcard span:nth-child(1){
      position: absolute;
      top: 0;
      left: 0;
      width: 100%;
      height: 3px;
      background: linear-gradient(to right, transparent,rgb(220, 27, 216));
      animation: animate1 2s linear infinite;
    }
    @keyframes animate1{
      0%{
        transform: translateX(-100%);
      }
      100%{
        transform: translateX(100%);
      }
    }

    .skillcard span:nth-child(2){
      position: absolute;
      top: 0;
      right: 0;
      width: 3px;
      height: 100%;
      background: linear-gradient(to bottom, transparent,rgb(220, 27, 216));
      animation: animate2 2s linear infinite;
      animation-delay: 1s;
    }
    @keyframes animate2{
      0%{
        transform: translateY(-100%);
      }
      100%{
        transform: translateY(100%);
      }
    }

    .skillcard span:nth-child(3){
      position: absolute;
      bottom: 0;
      left: 0;
      width: 100%;
      height: 3px;
      background: linear-gradient(to left, transparent,rgb(220, 27, 216));
      animation: animate3 2s linear infinite;
    }
    @keyframes animate3{
      0%{
        transform: translateX(100%);
      }
      100%{
        transform: translateX(-100%);
      }
    }

    .skillcard span:nth-child(4){
      position: absolute;
      top: 0;
      left: 0;
      width: 3px;
      height: 100%;
      background: linear-gradient(to top, transparent, rgb(220, 27, 216));
      animation: animate4 2s linear infinite;
      animation-delay: 1s;
    }
    @keyframes animate4{
      0%{
        transform: translateY(100%);
      }
      100%{
        transform: translateY(-100%);
      }
    }
    
    .scard{
      width:15rem
    }
  </style>
  