<template>
    <div class="testimonial" id="testimonial">
      <div class="container mt-5">
        <div class="row">
          <div class="col-md-4" v-for="(content, index) in skillContent" :key="content.title">
            <div class="card mb-3" v-if="index >= currentIndex && index < currentIndex + visibleItems">
              <div class="card-img-container" @click="toggleWords(content)">
                <img :src="content.picture" class="card-img" :alt="content.title" />
                <div class="words" v-if="content.showWords">
                  <p>{{ content.description }}</p>
                </div>
              </div>
              <div class="card-body">
                <h5 class="card-title">{{ content.title }}</h5>
              </div>
            </div>
          </div>
        </div>
        <button @click="prev" v-if="currentIndex > 0">Previous</button>
        <button @click="next" v-if="currentIndex + visibleItems < skillContent.length">Next</button>
      </div>
    </div>
  </template>
  
  <script>
  export default {
    data() {
      return {
        skillContent: [
          {
            picture: "https://i.postimg.cc/xdjQYvb5/icons8-html5-100.png",
            title: "HTML5",
            description: "Hypertext Markup Language, the standard markup language for documents designed to be displayed in a web browser.",
            showWords: false, // Initially, words are hidden
          },
          // ... (other skills)
        ],
        currentIndex: 0,
        visibleItems: 4, // Number of visible items in the carousel
      };
    },
    methods: {
      toggleWords(content) {
        content.showWords = !content.showWords; // Toggle the visibility
      },
      prev() {
        if (this.currentIndex > 0) {
          this.currentIndex -= 1;
        }
      },
      next() {
        if (this.currentIndex + this.visibleItems < this.skillContent.length) {
          this.currentIndex += 1;
        }
      },
    },
  };
  </script>
  
  <style scoped>
  .card-img-container {
    position: relative;
    cursor: pointer;
  }
  
  .card-img {
    transition: transform 0.5s;
  }
  
  .words {
    position: absolute;
    top: 0;
    left: 100%;
    background-color: white;
    border: 1px solid #ccc;
    padding: 10px;
    border-radius: 5px;
    display: none;
  }
  
  .card-img-container:hover .card-img {
    transform: scale(1.1);
  }
  
  .card-img-container:hover .words {
    display: block;
  }
  </style>
  