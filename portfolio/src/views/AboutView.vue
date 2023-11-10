<template>
  <div class="about" id="about">
    <div class="container">
      <section>
        <h1>About Me</h1>
        <p>
          I am a 21-year-old individual residing in Mitchell's Plain, having attended Meadowridge Primary School and Spine Road High School during my formative years. I pursued a three-year education at the Cape Peninsula University of Technology, although I did not complete my degree. Today, I am actively pursuing a childhood dream to exert a significant influence in the world of gaming, aiming to make a lasting impact.
        </p>
        <p>
          I am an ambitious and self-motivated individual with a strong desire to achieve personal greatness. I am unafraid to take risks in order to acquire new knowledge and skills. I thrive on meaningful interactions with individuals who can facilitate my self-improvement journey. My interests encompass reading, continuous learning in technology, maintaining physical fitness through regular exercise, and engaging in recreational gaming. Additionally, I value quality time spent in introspection to clear my mind of any negative thoughts that may impede my progress.
        </p>
      </section>
      <section>
        <h2>Hobbies</h2>
        <div class="row">
          <div v-for="content in hobbyContent" :key="content.title" class="col-md-4">
            <div class="card mb-3">
              <img :src="content.img" alt="" style="height: 15rem" class="card-img-top">
              <div class="card-body">
                <h3 class="card-title">{{ content.title }}</h3>
                <p>{{ content.one }}, {{ content.two }}, {{ content.three }}</p>
              </div>
            </div>
          </div>
        </div>
      </section>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      hobbyContent: [
        {
          img: "https://i.postimg.cc/76wj59ZX/top-10-books-every-college-student-read-1024x640.jpg",
          title: "Books",
          one: "Mystery",
          two: "Romance",
          three: "Fiction"
        },
        {
          img: "https://i.postimg.cc/CKVQ27kY/y5dxp8yemlzc8bypgfsl.jpg",
          title: "Games",
          one: "Horror",
          two: "JRPG",
          three: "Visual Novel"
        },
        {
          img: "https://i.postimg.cc/MpBLtNcd/adobestock-4437974.jpg",
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
  /* Add any additional styling here */
  section {
    margin-bottom: 2em;
  }

  h2, h3 {
    font-size: 1.5em;
  }
</style>
