<template>
  <div class="testimonial" id="testimonial">
    <h2 class="text-center">Peer Review</h2>
    <div class="torso">
      <div class="container contain2">
        <div class="contents-wraper" >
          <section class="content-row" @mouseover="pause" @mouseout="autoSliding">
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
              @mouseover="pause"
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
          review: 'Masood\'s determination and passion set him apart in IT. He meets deadlines with precision, excels in teamwork and solo work, adapts easily, and fosters inclusivity. He\'s an invaluable addition to any workplace.'
        },
        {
          name: 'Uzukhanye Dywil',
          image: 'https://i.ibb.co/BzpNDmX/C11-Uzukhanye-Dywili-4.jpg',
          review: 'Working with Masood Basardien was remarkable. His professionalism, attention to detail, and communication skills ensured seamless collaboration. He consistently exceeded expectations, delivering exceptional results. I wholeheartedly endorse him for anyone seeking a talented and dedicated professional.'
        },
        {
          name: 'Mujahid Fisher',
          image: 'https://i.ibb.co/x19FvdH/C12-C2-Mujahid-Fisher-3-11zon.jpg',
          review: 'Masood thinks independently and seeks help when needed. His ability to connect ideas, collaborate, and help others adds value to any company he joins.'
        },
        {
          name: 'Rabia Haucha',
          image: 'https://i.ibb.co/7t14RQT/LCA-Rabia-Haucha-Ju23-2.jpg',
          review: 'Masood Basardien is positive and dependable. His proactive work approach, commitment, and reliability make him a valuable team member. Masood\'s friendliness and effectiveness in group settings ensure smooth collaboration. It was a pleasure working with him, and I wholeheartedly recommend his services.'
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
padding-bottom:2rem;
padding-inline: 0.4rem;

}
.contain2{
  position: relative;
  width: 100%;
  min-height: 450px;    
  padding-bottom: 1.5rem;
  box-shadow: 0 0 0 2px #68e8ff, 8px 8px 0 0 #68e8ff;
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
  padding: 5px;
  color: white;
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
  background-color: #68e8ff;
  box-shadow: 1px 0px 10px 1px #68e8ff;
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
  .content-row .content-people img{
    width: 150px;
    height: 150px;
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
@media(max-width: 371px){
  .content-row .content-people p{
    font-size:14.8px;
  }
}

</style>
