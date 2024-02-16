<template>
  <div class="testimonial" id="testimonial">
    <h2 class="text-center mb-4">Peer Review</h2>
    <div class="torso">
      <div class="container contain2">
        <div class="contents-wraper" @mouseover="pause" @mouseout="autoSliding">
          <section class="content-row">
            <div v-for="(person, index) in people" :key="index" class="content-people" :class="{ active: index === activeIndex }">
              <img :src="person.image" >
              <h3>{{ person.name }}</h3>
              <p class="card-text">{{ person.review }}</p>
            </div>
          </section>

          <section class="indicators">
            <div
              v-for="(dot, index) in dots"
              :key="index"
              class="dot"
              :class="{ active: index === activeIndex }"
              @click="switchTest(index)"
            ></div>
          </section>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      people: [
        {
          name: 'Codi Kader',
          image: 'https://i.ibb.co/TB31Nmm/Codi-Kader-pfp.jpg',
          review: 'His unwavering determination and passion make him a standout talent in the IT sector. Masood consistently meets deadlines with precision and excels both in collaborative team settings and when working independently. His adaptable nature ensures success in any work environment, and his warm and welcoming demeanor fosters a sense of inclusivity, making him a truly invaluable addition to any workplace or business.'
        },
        {
          name: 'Uzukhanye Dywil',
          image: 'https://i.ibb.co/BzpNDmX/C11-Uzukhanye-Dywili-4.jpg',
          review: 'I had the privilege of working with Masood Basardien, and it was a truly remarkable experience. His unwavering professionalism, meticulous attention to detail, and excellent communication skills ensured a seamless and highly productive collaboration. Masood consistently exceeded my expectations, consistently delivering exceptional results. I wholeheartedly endorse Masood Basardien for anyone in search of a talented and dedicated professional.'
        },
        {
          name: 'Mujahid Fisher',
          image: 'https://i.ibb.co/x19FvdH/C12-C2-Mujahid-Fisher-3-11zon.jpg',
          review: 'Masood demonstrates an exceptional ability to think independently, seeking assistance when necessary. His adeptness at connecting ideas, collaborative skills, and readiness to assist others make him a valuable addition to any organization or industry he chooses to engage with.'
        },
        {
          name: 'Rabia Haucha',
          image: 'https://i.ibb.co/7t14RQT/LCA-Rabia-Haucha-Ju23-2.jpg',
          review: 'Masood Basardien is an exceptionally positive and dependable individual. His proactive approach to work, unwavering commitment to fulfilling his responsibilities, and strong reliability make him a valuable asset in any team. Masood\'s friendly disposition and effectiveness in group dynamics ensure a smooth collaborative experience. It was a pleasure working with him, and I wholeheartedly recommend his professional services.'
        },
        {
          name: 'Eighton Lee Paulse',
          image: 'https://i.ibb.co/x7YdTTm/Eighton-Lee-Paulse-pfp.jpg',
          
          review: 'Masood is a highly disciplined, sociable, and dedicated professional who thrives in both collaborative and independent work environments. He has successfully acquired proficiency in a range of web development technologies, including HTML, CSS, Bootstrap, JavaScript, MySQL, and VueJS, and his commitment to continuous learning promises further growth in the months ahead.'
        }
      ],
      dots: [0, 1, 2, 3, 4],
      activeIndex: 0,
      intervalId: null
    };
  },
  mounted() {
    this.autoSliding();
  },
  methods: {
    switchTest(index) {
      this.activeIndex = index;
      this.indicators();
    },
    slideNext() {
      if (this.activeIndex >= this.people.length - 1) {
        this.activeIndex = 0;
      } else {
        this.activeIndex++;
      }
      this.indicators();
    },
    autoSliding() {
      this.intervalId = setInterval(this.slideNext, 3000);
    },
    pause() {
      clearInterval(this.intervalId);
    },
    indicators() {
      }
  },
  beforeUnmount() {
    clearInterval(this.intervalId);
  }
};
</script>

<style>

.testimonial{
  padding-top: 5rem;
}
.torso{
width:100%;

display:flex;
justify-content: center;
align-items: center;
}
.contain2{
  position: relative;
  width: 100% !important;
  min-height: 450px;
  background:rgba(128, 128, 128, 0.471);
}
.contain2 .contents-wraper{
  width: 80%;
  min-height: inherit;
  margin: 30px auto;
  text-align: center;
}

.contents-wraper .content-row{
  width: 100%;
  min-height: inherit ;
  position: relative ;
  overflow: hidden;
}

.content-row .content-people{
  width: 100%;
  height: 100%;
  position: absolute;
  display: flex;
  justify-content: center;
  align-items: center;
  flex-direction: column;
}
.content-row .content-people:not(.active){
  top: 0;
  Left: -100%;
}
.content-row .content-people img{
  width: 200px;
  height: 200px;
  border-radius: 50%;
  object-fit: cover;
  margin-bottom: 5px;
  outline: 2px solid #006994;
  outline-offset: 2px;
}
.content-row .content-people h3{
  font-size:30px;
  font-style: italic;
  padding: 7px;
}
.content-row .content-people p{
  font-size: 18px;
  letter-spacing: 1px;
  line-height: 1.2;
  padding: 10px;
  color: white;
}

.contents-wraper .indicators{
  position: absolute;
  bottom: 30px;
  Left:50%;
  transform: translateX(-50%);
  padding: 5px;
  cursor: pointer;
}

.contents-wraper .indicators .dot{
  width:15px;
  height: 15px;
  margin: 0px 3px;
  border: 3px solid #aaa;
  border-radius: 50%;
  display:inline-block;
  transition: background-color 0.5s ease;
}

.contents-wraper .indicators .active{
  background-color: indigo;
  box-shadow: 1px 0px 10px 1px rgb(15, 0, 128);
}
@keyframes next1{
  from{
    Left:0%;
  }
  to{
    Left: -100%;
  }
} 
@keyframes next2{
  from{
    Left:100%;
  }
  to{
    Left: 0%;
  }
} 
@keyframes prev1{
  from{
    Left:0%;
  }
  to{
    Left: 100%;
  }
} 
@keyframes prev2{
  from{
    Left:-100%;
  }
  to{
    Left: 0%;
  }
}
@media(max-width: 550px){
  .contain2 .contents-wraper{
    width:90%;
  }
  .content-row .content-people h3{
    font-size: 26px;
  }
  .content-row .content-people p{
font-size:16px;
letter-spacing: initial;
line-height: initial;
  }
}
</style>
