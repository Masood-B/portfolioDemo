<template>
  <div class="home" id="home">
    <div class="content">
      <img class="self-pic" alt="myself" src="https://i.postimg.cc/bNfHQM6v/frontimage-1-removebg.png">
      <div class="text-content">
        <h2>Hello, I'm Masood Basardien</h2>
        <h2>An Aspiring Full-stack Web Developer</h2>
        <div>
          <button><a href="#about">About Me</a></button>
        </div>
      </div>
    </div>
  </div>
  <div>
    <AboutView/>
  </div>
  <div>
    <ResumeView/>
  </div>
  <div>
    <ProjectView/>
  </div>
  <div>
    <TestimonialView/>
  </div>
  <div>
    <ContactView/>
  </div>
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
  max-width: 100%;
  margin-right: 20px; 
}


@media (max-width: 769px) {
  .self-pic {
    display: none;
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
</style>