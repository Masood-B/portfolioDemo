<template>
  <div class="testimonial" id="testimonial">
    <div class="container">
      <h2 class="text-center mb-4">Testimonials</h2>
      <div class="row justify-content-center p-2">
        <div class="col-lg-10">
          <div id="testimonialCarousel" class="carousel slide" data-bs-ride="carousel" data-aos="flip-left"
          data-aos-easing="ease-out-cubic"
          data-aos-duration="2000">
            <div class="carousel-inner">
              <div
                class="carousel-item"
                v-for="(data, index) in testimonial"
                :key="index"
                :class="{ active: index === 0 }"
              >
                <div class="card animate__animated animate__flipInY animate__delay-1s">
                  <div class="row g-0">
                    <div class="col-md-4 img-box">
                      <img :src="data.image" class="img-fluid rounded-start img-fit" alt="..." loading="lazy">
                    </div>
                    <div class="col-md-8">
                      <div class="card-body">
                        <div class="top">
                          <h5 class="card-title">{{ data.name }}</h5>
                          <h5 class="card-title">{{ data.title }}</h5>
                        </div>
                        <div class="body-statement">
                          <p class="card-text">{{ data.statement }}</p>
                        </div>
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
             
            </a>
            <!-- <span class="visually-hidden">Previous</span> -->
            <a
              class="carousel-control-next"
              href="#testimonialCarousel"
              role="button"
              data-bs-slide="next"
            >
              <span class="carousel-control-next-icon" aria-hidden="true"></span>
        
            </a>
            <!-- <span class="visually-hidden">Next</span> -->
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
          image: "https://i.ibb.co/TB31Nmm/Codi-Kader-pfp.jpg",
          statement: "His unwavering determination and passion make him a standout talent in the IT sector. Masood consistently meets deadlines with precision and excels both in collaborative team settings and when working independently. His adaptable nature ensures success in any work environment, and his warm and welcoming demeanor fosters a sense of inclusivity, making him a truly invaluable addition to any workplace or business.",
        },
        {
          name: "Uzukhanye Dywili",
          image: "https://i.ibb.co/f1gvRbh/C11-Uzukhanye-Dywili-4.jpg",
          statement: "I had the privilege of working with Masood Basardien, and it was a truly remarkable experience. His unwavering professionalism, meticulous attention to detail, and excellent communication skills ensured a seamless and highly productive collaboration. Masood consistently exceeded my expectations, consistently delivering exceptional results. I wholeheartedly endorse Masood Basardien for anyone in search of a talented and dedicated professional.",
        },
        {
          name: "Mujahid Fisher",
          image: "https://i.ibb.co/gSq41hV/C12-C2-Mujahid-Fisher-3-11zon.jpg",
          statement: "Masood demonstrates an exceptional ability to think independently, seeking assistance when necessary. His adeptness at connecting ideas, collaborative skills, and readiness to assist others make him a valuable addition to any organization or industry he chooses to engage with.",
        },
        {
          name: "Rabia Haucha",
          image: "https://i.ibb.co/7t14RQT/LCA-Rabia-Haucha-Ju23-2.jpg",
          statement: "Masood Basardien is an exceptionally positive and dependable individual. His proactive approach to work, unwavering commitment to fulfilling his responsibilities, and strong reliability make him a valuable asset in any team. Masood's friendly disposition and effectiveness in group dynamics ensure a smooth collaborative experience. It was a pleasure working with him, and I wholeheartedly recommend his professional services.",
        },
        {
          name: "Eighton Lee Paulse",
          image: "https://i.ibb.co/wz7jmmJ/Eighton-Lee-Paulse-pfp.jpg",
          statement: "Masood is a highly disciplined, sociable, and dedicated professional who thrives in both collaborative and independent work environments. He has successfully acquired proficiency in a range of web development technologies, including HTML, CSS, Bootstrap, JavaScript, MySQL, and VueJS, and his commitment to continuous learning promises further growth in the months ahead.",
        }
      ],
    };
  },
};
</script>

<style>
.testimonial {
  font-size: 1.5vw;
}


@media (max-width: 768px) {
  .testimonial {
    font-size: 2vw;
  }
  .img-fit {
    max-width: 80%; 
  }
}

@media (max-width: 576px) {
  .testimonial {
    font-size: 3vw;
  }
  .img-fit {
    max-width: 60%; 
  }
}

.testimonial{
  padding-top: 5rem;
}
.carousel-inner{
  margin-top: 5rem;
}
.carousel-control-next{
  width:2rem !important;
}
.carousel-control-next-icon{
 background-image: none !important;

}

.carousel-control-prev{
  width:2rem !important;
}
.carousel-control-prev-icon{
  background-image: none !important;
 }
 .body-statement{
  margin:0  5rem
 }

</style>
