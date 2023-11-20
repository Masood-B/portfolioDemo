<template>
    <div>
      <nav class="navbar navbar-expand-lg bg-color fixed-top">
        <div class="container-fluid">
          <button
            class="navbar-toggler"
            type="button"
            data-bs-toggle="collapse"
            data-bs-target="#navbarSupportedContent"
            aria-controls="navbarSupportedContent"
            aria-expanded="false"
            aria-label="Toggle navigation"
          >
            <span class="navbar-toggler-icon"></span>
          </button>
          <div class="collapse navbar-collapse" id="navbarSupportedContent">
            <ul class="navbar-nav mx-auto"> <!-- Center the navbar links -->
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
    methods: {
    }
}
</script>

<style scoped>
.bg-color {
    background-color: rgba(0, 0, 0, 0.148);
}
.nav-link{
  color: white;
}
.nav-link:hover{
  color: brown
}
</style>