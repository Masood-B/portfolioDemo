<template>
    <div class="resume" id="resume">
      <div class="container">
        <section>
          <h2>Education</h2>
          <div class="card cardd" v-for="content in educationContent" :key="content.year">
            <img src="" alt="">
            <h4>{{ content.year }}</h4>
            <div class="card-body">
              <p>{{ content.description }}</p>
            </div>
          </div>
        </section>
  
        <section>
          <h2>Skills</h2>
          <div class="row">
            <div class="col-md-3" v-for="content in skillContent" :key="content.title">
              <div class="card mb-3 skillcard">
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
            description: "Studied coding at Life Choice Academy for 6 months"
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
            picture: "https://i.postimg.cc/gcxkPjVK/icons8-html-480.png",
            title: "HTML5"
          },
          {
            picture: "https://i.postimg.cc/SRnKTNrD/icons8-css-480.png",
            title: "CSS3"
          },
          {
            picture: "https://i.postimg.cc/d32NLfby/icons8-bootstrap-144.png",
            title: "Bootstrap"
          },
          {
            picture: "https://i.postimg.cc/NjMbcLjT/icons8-javascript-144.png",
            title: "JavaScript"
          },
          {
            picture: "https://i.postimg.cc/V6zWwQ9B/icons8-vue-js-240.png",
            title: "Vue.js"
          },
          {
            picture: "https://i.postimg.cc/3w8qkJZS/icons8-mysql-480.png",
            title: "MySQL"
          }
        ]
      };
    }
  };
  </script>
  
  <style scoped>
    /* Add any additional styling here */
    section {
      margin-bottom: 2em;
    }
  
    .cardd {
      margin: 5px 0;
      border-radius: 20px;
      padding: 5px;
      width: 50%;
      border: 2px solid black;
      background: orange;
    }
  
    .cardd:nth-child(odd) {
      box-shadow: 0.5vw 0.2vw 0.7vw;
    }
  
    .cardd:nth-child(even) {
      box-shadow: 0.5vw 0.2vw 0.7vw;
      margin-left: auto;
    }
  
    @media screen and (max-width: 900px) {
      .cardd {
        width: 100%;
        flex-wrap: wrap;
      }
  
      .cardd a,
      .cardd p,
      footer p {
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
  </style>
  