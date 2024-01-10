<template>
  <div class="about" id="about">
    <div class="container">
      <div class="row">
        <div class="col-md-6">
          <section data-aos="fade-right">
            <h2>About Me</h2>
            <p>
              I am a 21-year-old individual residing in Mitchell's Plain, having attended Meadowridge Primary School and Spine Road High School during my formative years. I pursued a three-year education at the Cape Peninsula University of Technology, although I did not complete my degree. Today, I am actively pursuing a childhood dream to exert a significant influence in the world of gaming, aiming to make a lasting impact.
            </p>
            <p>
              I am an ambitious and self-motivated individual with a strong desire to achieve personal greatness. I am unafraid to take risks in order to acquire new knowledge and skills. I thrive on meaningful interactions with individuals who can facilitate my self-improvement journey. My interests encompass reading, continuous learning in technology, maintaining physical fitness through regular exercise, and engaging in recreational gaming. Additionally, I value quality time spent in introspection to clear my mind of any negative thoughts that may impede my progress.
            </p>
          </section>
        </div>
        <div class="col-md-6">
          <section data-aos="fade-left">
            <h2>Hobbies</h2>
            <div class="row">
              <div v-for="content in hobbyContent" :key="content.title" class="col-md-6">
                <h3>{{ content.title }}</h3>
                <ul class="list-unstyled circle-list">
                  <li>{{ content.one }}</li>
                  <li>{{ content.two }}</li>
                  <li>{{ content.three }}</li>
                </ul>
              </div>
            </div>
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
      hobbyContent: [
        {
          title: "Books",
          one: "Mystery",
          two: "Romance",
          three: "Fiction"
        },
        {
          title: "Games",
          one: "Horror",
          two: "JRPG",
          three: "Visual Novel"
        },
        {
          title: "Sports",
          one: "Basketball",
          two: "Cricket",
          three: "Golf"
        }
      ]
    };
  },
  components: {}
};
</script>

<style scoped>
section {
  margin-bottom: 2em;
}

h3 {
  font-size: 1.5em;
}

h3, p, li {
  color: black;
}

.circle-list {
  list-style-type: none;
  padding-left: 0;
}

.circle-list li {
  position: relative;
  margin-bottom: 10px;
  text-align: left;
}

.circle-list li:before {
  content: '\2022';
  display: inline-block;
  width: 1rem;
  height: 1rem;
  line-height: 1rem;
  text-align: center;
  border: 1px solid #000;
  border-radius: 50%;
  margin-right: 10px;
  background-color: #000000; /* You can change the background color as needed */
}
.about{
padding-top: 5rem;
}
h2{
  padding-bottom:2rem;
}
</style>