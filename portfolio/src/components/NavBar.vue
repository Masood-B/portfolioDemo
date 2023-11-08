<template>
    <div>
        <nav class="navbar navbar-expand-lg bg-body-tertiary">
  <div class="container-fluid">
    <router-link to="/"><img src="https://steamuserimages-a.akamaihd.net/ugc/773973896821782037/EA53BD5AA7AC510606C0884B91FC204506946FC3/?imw=5000&imh=5000&ima=fit&impolicy=Letterbox&imcolor=%23000000&letterbox=false" alt="Logo"></router-link>
    <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarSupportedContent" aria-controls="navbarSupportedContent" aria-expanded="false" aria-label="Toggle navigation">
      <span class="navbar-toggler-icon"></span>
    </button>
    <div class="collapse navbar-collapse" id="navbarSupportedContent">
      <ul class="navbar-nav ms-auto mb-2 mb-lg-0">
        <li class="nav-item">
        <a class="nav-link" href="#">Home</a>
        </li>
        <li class="nav-item">
     <a class="nav-link" href="#about">About</a>
        </li>
        <li class="nav-item">
     <a class="nav-link" href="#resume">Resume</a>
        </li>
        <li class="nav-item">
     <a class="nav-link" href="#project">Project</a>
        </li>
        <li class="nav-item">
     <a class="nav-link" href="#testimonial">Testimonial</a>
        </li>
        <li class="nav-item">
     <a class="nav-link" href="#contact">Contact</a>
        </li>
      </ul>
    </div>
  </div>
</nav>
    </div>
</template>

<script>
    export default {
        methods:{
          scrollTop(){
            document.body.scrollTop = document.documentElement.scrollTop = 0;
          }
        }
    }
</script>

<style scoped>

</style>