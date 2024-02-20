<template>
  <div class="project" id="project">
    <div class="container">
      <h2>Project</h2>
      <div class="row">
        <div class="col-md-4 mx-auto" v-for="content in projectContent" :key="content.title" data-aos="fade-up"
        data-aos-duration="1000">
          <div class="card mb-3">
            <div class="card-img-container">
              <img :src="content.picture" class="card-img" :alt="content.title">
              <div class="overlay">
                <a :href="content.code" target="_blank"><button>Code</button></a>
                <a :href="content.live" target="_blank"><button>Live</button></a>
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
                projectContent: [
                  {
                    picture: "https://wallpapercave.com/wp/wp2497495.jpg",
                    title: "Simple Calculator",
                    code:"https://github.com/Masood-B/calculatorProject",
                    live:"https://idyllic-sfogliatella-dc6519.netlify.app/"
                  },
                  {
                    picture: "https://cdn1.byjus.com/wp-content/uploads/2019/03/relation-between-celsius-and-fahrenheit.png",
                    title: "Temperature",
                    code:"https://github.com/Masood-B/temperatureProject",
                    live:"https://phenomenal-dasik-09db32.netlify.app/"
                  },
                  {
                    picture: "https://i.ibb.co/dDQWMyP/Screenshot-2024-02-19-111123.png",
                    title: "Old Portfolio",
                    code:"https://github.com/Masood-B/vuePortfolioProject",
                    live:"https://vue-portfolio-61517.firebaseapp.com/"
                  },
                  {
                    picture: "https://t3.ftcdn.net/jpg/02/23/57/42/360_F_223574261_LmzlzkLtjR0cxcDNvkmr2xHfMU69CheO.jpg",
                    title: "BMI Calculator",
                    code:"https://github.com/Masood-B/CalculatorBMIproject",
                    live:"https://luxury-melba-07ed58.netlify.app/"
                  },
                  {
                    picture: "https://capstonewriting.com/wp-content/uploads/2020/08/blog_img2-1200x900.jpg",
                    title: "Capstone",
                    code:"https://github.com/Masood-B/capstoneProject/tree/main",
                    live:"https://capstoneeomp.web.app/"
                  }
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
            transition: filter 0.5s;
          }

          img{
            height: 15rem;
          }
          
          .overlay {
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background-color: rgba(0, 0, 0, 0.7);
            opacity: 0;
            transition: opacity 0.25s;
            display: flex;
            justify-content:space-evenly;
            align-items:end;
            
          }

          /*.overlay--blur{
            backdrop-filter: blur(1px);
          }*/

          .overlay > * {
            transform:translateY(20px);
            transition: transform 0.25s;
          }
          
          .overlay button {
            font-family: "Open Sans", sans-serif;
            font-size: 16px;
            letter-spacing: 2px;
            text-decoration: none;
            text-transform: uppercase;
            color: #000;
            cursor: pointer;
            border: 3px solid;
            padding: 0.25em 0.5em;
            box-shadow: 1px 1px 0px 0px, 2px 2px 0px 0px, 3px 3px 0px 0px, 4px 4px 0px 0px, 5px 5px 0px 0px;
            position: relative;
            user-select: none;
            touch-action: manipulation;
          }

          .overlay button:active {
            box-shadow: 0px 0px 0px 0px;
            top: 5px;
            left: 5px;
          }
          
          .card-img-container:hover .card-img {
            filter:grayscale(100%)
          }
          
          .card-img-container:hover .overlay {
            opacity: 1;
          }

          .card-img-container:hover .overlay > *{
            transform: translateY(0);
          }
          .project{
            padding-top: 5rem;
            background-image: url(https://i.ibb.co/xXpGcGd/neon-city-retro-music-synthwave-1920x1080-wallpx-com.jpg);
            background-size:100vw 100vh;
            background-repeat:no-repeat;
            background-position: center center;
            background-attachment: fixed;
          }
          h2{
            padding-bottom: 2rem;
          }
          .card{
            background: rgb(71, 70, 67);
          }

          @media (min-width: 768px) {
            .overlay button {
              padding: 0.25em 0.75em;
            }
          }

          .col-md-4{
            width: 21rem;
          }
          .card-body{
           color: rgb(244, 245, 247) ;
          }
          </style>
          