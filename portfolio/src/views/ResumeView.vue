<template>
    <div class="resume" id="resume">
        <div class="container">
        <h2>Education</h2>
        <div class="card" v-for="content in educationContent" :key="content">
            <h4>{{content.year}}</h4>
            <div class="card-body">
                <p>{{ content.description }}</p>
            </div>
        </div>
        <div>
            <h2>Skill</h2>
            <div class="row">
                <div class="col-md-3" v-for="content in skillContent" :key="content.title">
                  <div class="card mb-3 skillcard">
                    <img :src="content.picture" class="card-img-top" alt="{{ content.title }}">
                    <div class="card-body">
                      <h2 class="card-title">{{ content.title }}</h2>
                    </div>
                  </div>
                </div>
              </div>
        </div>
</div>
    </div>
</template>

<script>
    export default {
        data(){
            return{
                educationContent:[
                    {
                        year:"2023",
                        description:"I studied coding at Life Choice Academy for 6 month"
                    },
                    {
                        year:"2020-2022",
                        description:"I went to Cape Peninsula University of Technology to study Biotechnology and didnt finish to get my degree"
                    },
                    {
                        year:"2015-2019",
                        description:"I matriculated at Spine Road High School with a bachelor pass"
                    }
                ],
                skillContent:[
                    {
                        picture: "https://i.postimg.cc/gcxkPjVK/icons8-html-480.png",
                        title: "HTLM5"
                    },
                    {
                        picture: "https://i.postimg.cc/SRnKTNrD/icons8-css-480.png",
                        title: "CSS3"
                    },
                    {
                        picture: "https://i.postimg.cc/d32NLfby/icons8-bootstrap-144.png",
                    title: "Bootstrap",
                    },
                    {
                        picture: "https://i.postimg.cc/NjMbcLjT/icons8-javascript-144.png",
                        title: "JavaScript"
                    },
                    {
                        picture: "https://i.postimg.cc/V6zWwQ9B/icons8-vue-js-240.png",
                        title: "Vue.js"
                    },
                    {
                        picture:"https://i.postimg.cc/3w8qkJZS/icons8-mysql-480.png",
                        title:"MySQL"
                    }
                ]
            }
        }
    }
</script>

<style scoped>
.card-bottom {
    padding: 1rem;
  }
  
  .card-bottom h5 {
    font-weight: bold;
  }
  
  
</style>