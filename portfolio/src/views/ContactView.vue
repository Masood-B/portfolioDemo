<template>
    <div class="contact" id="contact">
        <div class="container">
        <div class="row">
            <div class="col-12">
              <h2>Contact Us</h2>
            </div>
            <div class="col-12 col-md-6 mb-4">
              <img
                src="https://i.postimg.cc/2y2rFq47/anime-wallpaper-7628310-1280.webp"
                class="img-fluid"
                alt=""
              />
            </div>
            <div class="col-12 col-md-6">
              <form
                action="https://formspree.io/f/xbjewvba"
                class="w-100"
                method="POST"
              >
                <div class="mb-3">
                  <label for="name" class="form-label">Name</label>
                  <input
                    type="text"
                    name="name"
                    class="form-control"
                    id="name"
                    placeholder="Your Name"
                    required
                  />
                </div>
                <div class="mb-3">
                  <label for="surname" class="form-label">Surname</label>
                  <input
                    type="text"
                    name="Surname"
                    class="form-control"
                    id="surname"
                    placeholder="Your Surname"
                    required
                  />
                </div>
                <div class="mb-3">
                  <label for="email" class="form-label">Email address</label>
                  <input
                    type="email"
                    name="email"
                    class="form-control"
                    id="email"
                    placeholder="Your Email"
                    required
                  />
                </div>
                <div class="mb-3">
                  <label for="message" class="form-label">Message</label>
                  <textarea
                    class="form-control"
                    name="message"
                    id="message"
                    rows="3"
                    placeholder="Write Here"
                    required
                  ></textarea>
                </div>
                <div class="mb-3">
                  <button class="btn btn-primary">Submit</button>
                </div>
              </form>
            </div>
          </div>
        </div>
        </div>
          </template>
          
          <script>
          export default {

          };
          </script>
          
          <style>
         
          </style>
          