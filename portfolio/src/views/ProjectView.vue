<template>
    <div class="project" id="project">
        
            <div class="container">
                <h2>Project</h2>
              <div class="row">
                <div class="col-md-4" v-for="content in skillContent" :key="content.title">
                  <div class="card mb-3">
                    <div class="card-img-container">
                      <img :src="content.picture" class="card-img" alt="{{ content.title }}">
                      <div class="overlay">
                        <div class="text"><button>RED</button></div>
                        <div class="text"><button>BLUE</button></div>
                      </div>
                    </div>
                    <div class="card-body">
                      <h5 class="card-title">{{ content.title }}</h5>
                    </div>
                  </div>
                </div>
              </div>
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
                    description: "I studied coding at Life Choice Academy for 6 months",
                  },
                  {
                    year: "2020-2022",
                    description: "I went to university to study Biotechnology and didn't finish to get my degree",
                  },
                  {
                    year: "2015-2019",
                    description: "I matriculated at Spine Road High School with a bachelor pass",
                  },
                ],
                skillContent: [
                  {
                    picture: "https://i.postimg.cc/xdjQYvb5/icons8-html5-100.png",
                    title: "HTML5",
                  },
                  {
                    picture: "https://i.postimg.cc/76fyJq9T/icons8-css3-100.png",
                    title: "CSS3",
                  },
                  {
                    picture: "https://i.postimg.cc/d32NLfby/icons8-bootstrap-144.png",
                    title: "Bootstrap",
                  },
                  {
                    picture: "https://i.postimg.cc/NjMbcLjT/icons8-javascript-144.png",
                    title: "JavaScript",
                  },
                  {
                    picture: "https://i.postimg.cc/V6zWwQ9B/icons8-vue-js-240.png",
                    title: "Vue.js",
                  },
                  {
                    picture: "https://i.postimg.cc/3w8qkJZS/icons8-mysql-480.png",
                    title: "MySQL",
                  },
                ],
              };
            },
          };
          </script>
          
          <style scoped>
          .card-img-container {
            position: relative;
            overflow: hidden;
          }
          
          .card-img {
            transition: transform 0.5s;
          }
          
          .overlay {
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background-color: rgba(0, 0, 0, 0.7);
            opacity: 0;
            transition: opacity 0.5s;
            display: flex;
            justify-content: center;
            align-items: center;
          }
          
          .text {
            color: white;
            font-size: 24px;
            font-weight: bold;
          }
          
          .card-img-container:hover .card-img {
            transform: scale(1.1);
          }
          
          .card-img-container:hover .overlay {
            opacity: 1;
          }
          </style>
          