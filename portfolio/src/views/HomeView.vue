<template>  
  <div class="home" id="home">
    <div class="content">
      <div class="image-container">
        <img class="self-pic" alt="myself" src="https://i.ibb.co/fGSzy6h/frontimage-1-removebg.png"  border="0" loading="lazy" />
        <div class="image-overlay"></div>
      </div>
      <div class="text-content" data-aos="fade-down"
      data-aos-easing="linear"
      data-aos-duration="1500">
        <h2>Hello, I'm Masood Basardien</h2>
        <h2>An Aspiring Full-stack Web Developer</h2>
        <div>
          <a href="#about"><button class="aboutButton">About Me</button></a>
        </div>
      </div>
    </div>
  </div>
  <section>
    <AboutView/>
  </section>
  <section>
    <ResumeView/>
  </section>
  <section>
    <ProjectView/>
  </section>
  <section>
    <TestimonialView/>
  </section>
  <section>
    <ContactView/>
  </section>
  <footer class="footer">
    <div class="container text-center">
      <p>CopyRight &copy; {{ cYear }} Masood Basardien</p>
    </div>
  </footer>
</template>

<script>
import AboutView from './AboutView.vue';
import ResumeView from './ResumeView.vue';
import ProjectView from './ProjectView.vue';
import TestimonialView from './TestimonialView.vue';
import ContactView from './ContactView.vue';
export default {
  components: {
    AboutView,
    ResumeView,
    ProjectView,
    TestimonialView,
    ContactView
  },
  data() {
    return {
      cYear: new Date().getUTCFullYear(),
    };
  }
}
</script>

<style>
.content {
  display: flex;
  justify-content: center;
  align-items: center;
  height: 100vh; 
  padding: 2rem;
}
h2{
  color: white !important;
}

.aboutButton {
  background-color: #a5aaf9;
  border-radius: 100px;
  box-shadow: rgba(14, 200, 233, 0.2) 0 -25px 18px -14px inset,rgba(14, 200, 233, 0.2) 0 8px 16px,rgba(14, 200, 233, 0.2) 0 16px 32px;
  color: rgb(57, 195, 246);
  cursor: pointer;
  display: inline-block;
  font-family: CerebriSans-Regular,-apple-system,system-ui,Roboto,sans-serif;
  padding: 7px 20px;
  text-align: center;
  text-decoration: none;
  transition: all 250ms;
  border: 0;
  font-size: 16px;
  user-select: none;
  -webkit-user-select: none;
  touch-action: manipulation;
}
a .aboutButton{
  text-decoration: none;
  color: black  ;
}
a .aboutButton:hover{
  color: rgb(24, 37, 30) ;
}

.aboutButton:hover {
  box-shadow: rgba(136, 1, 247, 0.456) 0 -25px 18px -14px inset,rgba(1, 242, 247, 0.456) 0 1px 2px,rgba(1, 242, 247, 0.456) 0 2px 4px,rgba(1, 242, 247, 0.456) 0 4px 8px,rgba(1, 242, 247, 0.456) 0 8px 16px,rgba(1, 242, 247, 0.456) 0 16px 32px;
  transform: scale(1.05) rotate(-1deg);
  background-color: rgba(17, 214, 201, 0.725);
}

.centered {
  text-align: center;
}

.self-pic {
  min-width: 30%;
  margin-right: 20px;
  position: relative;
  z-index: 1;
}


.image-container {
  position: relative;
  display: inline-block;
}


.image-container img {
  display: block;
  max-width: 100%;
  height: auto;
}


.image-overlay {
  position: absolute;
  top: 13%;
  right: 5%;
  width: 100%;
  height: 90%;
  background-color: #2d3d64b9;
  z-index: 0; 
  transform: skewY(-5deg);
}

@media (max-width: 768px) {
  .self-pic {
    display: none !important;
  }

  .image-overlay {
    display: none ;
  }
}

@media (max-width: 768px) {
  .content {
    flex-direction: column; 
    text-align: center;
  }

  .self-pic {
    margin-right: 0; 
  }

  .home h2 {
    font-size: 1.5rem;
  }

  .home button {
    font-size: 1rem;
  }
}

.footer {
  background-color: #242b33;
  padding: 5px 0;
  bottom: 0;
  width: 100%;
}

</style>