<template>
  <div class="home" id="home">
    <img class="self-pic" alt="myself" src="https://i.postimg.cc/bNfHQM6v/frontimage-1-removebg.png">
    <div>
      <h2>Hello, I'm Masood Basardien</h2>
      <h2>An Aspiring Full-stack Web Developer</h2>
      <div>
        <button><a href="#about">About Me</a></button>
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
