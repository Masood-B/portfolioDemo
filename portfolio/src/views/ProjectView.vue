<template>
  <div class="project" id="project">
    <div class="container">
      <h2>Project</h2>
      <div class="row">
        <div class="col-md-3 mx-auto" v-for="content in projectContent" :key="content.title">
          <div class="card mb-3">
            <div class="card-img-container">
              <img :src="content.picture" class="card-img" alt="{{ content.title }}">
              <div class="overlay">
                <div class="text"><button>Code</button></div>
                <div class="text"><button>Live</button></div>
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
                    picture: "https://mcdn.wallpapersafari.com/medium/47/59/CbeI43.jpg",
                    title: "1",
                  },
                  {
                    picture: "https://mcdn.wallpapersafari.com/medium/47/59/CbeI43.jpg",
                    title: "2",
                  },
                  {
                    picture: "https://mcdn.wallpapersafari.com/medium/47/59/CbeI43.jpg",
                    title: "3",
                  },
                  {
                    picture: "https://mcdn.wallpapersafari.com/medium/47/59/CbeI43.jpg",
                    title: "4",
                  },
                  {
                    picture: "https://mcdn.wallpapersafari.com/medium/47/59/CbeI43.jpg",
                    title: "5",
                  },
                  {
                    picture: "https://mcdn.wallpapersafari.com/medium/47/59/CbeI43.jpg",
                    title: "6",
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
            justify-content:space-between;
            align-items:end;
          }
          
          .text {
            font-size: 20px;
            font-weight: bold;
          }
          
          .card-img-container:hover .card-img {
            transform: scale(1.1);
          }
          
          .card-img-container:hover .overlay {
            opacity: 1;
          }
          .project{
            padding-top: 5rem;
          }
          h2{
            padding-bottom: 2rem;
          }
          .card{
            background: rgb(71, 70, 67);
          }
          </style>
          