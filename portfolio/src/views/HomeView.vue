<template>  
  <div class="home" id="home">
    <div class="content">
      <div class="image-container">
        <img class="self-pic" alt="myself" src="https://i.ibb.co/fGSzy6h/frontimage-1-removebg.png"  border="0" loading="lazy"/>
        <div class="image-overlay"></div>
      </div>
      <div class="text-content">
        <h2>Hello, I'm Masood Basardien</h2>
        <h2>An Aspiring Full-stack Web Developer</h2>
        <div>
          <button><a href="#about" class="aboutButton">About Me</a></button>
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
  <footer class="footer mt-5">
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
  top: 20%;
  right: 5%;
  width: 90%;
  height: 80%;
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