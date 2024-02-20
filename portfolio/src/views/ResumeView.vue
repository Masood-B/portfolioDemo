
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
          <div class="row centercard">
            <div class="scard" v-for="content in skillContent" :key="content.title" >
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

        <section>
          <h2>Certificate/Badge</h2>
          <div class="row centercard">
            <div class="scard" v-for="content in badgeContent" :key="content.title" >
              <div class="mb-3" data-aos="flip-down">
                <a :href="content.site" target="_blank"><img :src="content.picture" class="card-img-top" alt="{{ content.title }}"></a>
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
            picture: "https://i.ibb.co/THPcVy5/nodejso.png",
            title: "Node JS"
          },
          {
            picture: "https://i.ibb.co/nR9jFbn/icons8-mysql-480.png",
            title: "Vue.js"
          },
          {
            picture: "https://i.ibb.co/ZTHTmPg/icons8-vue-js-480.png",
            title: "MySQL"
          },
          {
            picture: "https://i.ibb.co/R3rFFJ4/rest-api-blue-logo-22098.png",
            title: "REST API"
          },
        ],badgeContent:[{
          picture:"https://images.credly.com/size/220x220/images/dcdf1a3c-2594-4f4c-a33a-050b4bca58b5/image.png",
          site:"https://www.credly.com/badges/62023fb5-846a-4b85-aaea-b172437544f8/public_url"
        },{
          picture:"https://images.credly.com/size/220x220/images/8d67bbf4-128b-4141-b5f1-1bc61bbfbaa6/image.png",
          site:"https://www.credly.com/badges/a4c81273-1ac7-45f4-975f-8f558dfeff3b/public_url"
        },{
          picture:"https://images.credly.com/size/220x220/images/5bdd6a39-3e03-4444-9510-ecff80c9ce79/image.png",
          site:"https://www.credly.com/badges/cc5dcd92-e992-4c3b-8c54-1c639dea657a/public_url"
        },{
          picture:"https://images.credly.com/size/220x220/images/af8c6b4e-fc31-47c4-8dcb-eb7a2065dc5b/I2CS__1_.png",
          site:"https://www.credly.com/badges/395426c7-c70a-4044-8168-83e6d727f8bc/public_url"
        },{
          picture:"https://images.credly.com/size/220x220/images/978f88dc-c247-4093-9d39-6efac3651297/image.png",
          site:"https://www.credly.com/badges/eaceecdd-a73f-4a9a-bc99-ebb0d991f755/public_url"
        },{
          picture:"https://images.credly.com/size/220x220/images/441578ec-c0f3-46cc-95fc-86b27e90cf4f/image.png",
          site:"https://www.credly.com/badges/94f99893-7a05-4d9a-8cdc-bc4b092a7b23/public_url"
        },{
          picture:"https://images.credly.com/size/220x220/images/68c0b94d-f6ac-40b1-a0e0-921439eb092e/image.png",
          site:"https://www.credly.com/badges/a0eaeab6-ca0f-4475-bf97-6037565ec26b/public_url"
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
      background-image:  url(https://i.pinimg.com/564x/ec/8d/25/ec8d25482761bfde2357382a52b13f14.jpg) ;
      background-size:50%;
      background-position: center;
    }
    .cardd p, h4{
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
      color:white !important;
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
      width:15rem;
      display: flex;
      justify-content: center;
      align-items: center;
    }

    .centercard{
      display: flex;
      justify-content: center;
      align-items: center;
    }
    h3{
      color: rgb(244, 245, 247);
    }
  </style>
  