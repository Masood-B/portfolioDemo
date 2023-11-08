<template>
    <div class="testimonial" id="testimonial">
      <div class="container">
        <h2 class="text-center mb-4">Testimonials</h2>
        <div class="row justify-content-center p-2">
          <div class="col-lg-10">
            <div id="testimonialCarousel" class="carousel slide" data-bs-ride="carousel">
              <div class="carousel-inner">
                <div
                  class="carousel-item"
                  v-for="(data, index) in testimonial"
                  :key="index"
                  :class="{ active: index === 0 }"
                >
                  <div class="card animate__animated animate__flipInY animate__delay-1s">
                    <div class="row g-0">
                      <div class="col-md-4">
                        <img :src="data.image" class="img-fluid rounded-start img-fit" alt="..." loading="lazy" style="height:38rem">
                      </div>
                      <div class="col-md-8">
                        <div class="card-body">
                          <h5 class="card-title">{{ data.name }}</h5>
                          <p class="card-text">{{ data.statement }}</p>
                        </div>
                      </div>
                    </div>
                  </div>
                </div>
              </div>
              <a
                class="carousel-control-prev"
                href="#testimonialCarousel"
                role="button"
                data-bs-slide="prev"
              >
                <span class="carousel-control-prev-icon" aria-hidden="true"></span>
                <span class="visually-hidden">Previous</span>
              </a>
              <a
                class="carousel-control-next"
                href="#testimonialCarousel"
                role="button"
                data-bs-slide="next"
              >
                <span class="carousel-control-next-icon" aria-hidden="true"></span>
                <span class="visually-hidden">Next</span>
              </a>
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
        testimonial: [
          {
            name: "Codi Kader",
            image: "https://i.postimg.cc/7h0yrP5d/Codi-Kader-pfp.jpg",
            statement: "Masood Basardien, He is a very determined, passionate and kind young man. He is going to do great things in the IT sector. You can count on that. Masood strives his best to make sure that all his deadlines & work is done as soon as possible and correctly as possible. He works really well in a group or alone. He is able to adapt in any environment he is placed in. Once you get to know him you feel a sense of belonging as he is able to welcome you in with a warm and kind atmosphere. This is a great addition to any workplace or business."
          },
          {
            name: "Mogammad Imtiyaaz Damon",
            image:"https://i.postimg.cc/pLDM6LwF/Mogammad-Damon-pfp.jpg",
            statement:"Masood is a kind person with a great sense of humour. He is a great friend and he is very intelligent."
          },
          {
            name: "Uzukhanye Dywili",
            image:"https://i.postimg.cc/hvDWNMzZ/C11-Uzukhanye-Dywili-4.jpg",
            statement:"Working with Masood Basardien was an incredible experience. Their professionalism, attention to detail, and communication skills made the entire process seamless. They consistently exceeded my expectations and delivered exceptional results. I would highly recommend Masood Basardien to anyone looking for a talented and dedicated professional."
          },
          {
            name: "Taflynne Summer Petersen",
            image:"https://i.postimg.cc/W4yPWMSj/Taflynne-Summer-Petersen-pfp.jpg",
            statement:"Masood Basardien is a good person to work with, he thinks for himself and asks for help when needed only. He is good at putting two and two together, works well in a group setting and is very helpful. He is an asset to any company or field he pursues."
          },
          {
            name: "Eighton Lee Paulse",
            image:"https://i.postimg.cc/4NSDd9gt/Eighton-Lee-Paulse-pfp.jpg",
            statement:"Masood Basardien is a very positive individual. He often tries his best to help with work and does his part in everything the way he needs to do. He is very reliable and friendly and works well in groups. My experience working with him was great. I would definitely recommend him."
          },
          {
            name: "Joel Mukanya",
            image:"https://i.postimg.cc/HnybG6gL/Joel-Profile.jpg",
            statement:"Masood is very well-behaved, social, and dedicated; he enjoys working with his peers and works well on his project. He learned HTML, CSS, Bootstrap, and VueJS. He will learn more in the coming months."
          }
        ],
      };
    },
  };
  </script>
  
  <style>
  /* Add custom CSS styles here if needed */
  </style>
  