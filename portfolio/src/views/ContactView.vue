<template>
    <div class="contact" id="contact">
        <div class="container">
          <h2>Contact Us</h2>
        <div class="row">
            <div class="col">
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
                  <button class="button" role="button"><span class="text">Press</span><span>Submit</span></button>
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
.contact{
  padding-top: 5rem;
  background-image: url(https://i.ibb.co/h8YDfhd/wallpaperflare-com-wallpaper-3.jpg);
  background-size:100vw 100vh;
  background-repeat:no-repeat;
  background-position: center center;
  background-attachment: fixed;
  display:flex;
justify-content: center;
align-items: center;
}  
h2{
  padding-bottom: 2rem;
}     
label{
  color: white;
}
input, textarea{
  background: rgba(9, 0, 0, 0.447) !important;
  color:white !important;
  border: rgb(10, 163, 234) solid 1px !important;
  border-radius: 1rem !important;
  
}
::placeholder{
  color: white !important;
}

.button {
  position: relative;
  overflow: hidden;
  border: 2px solid rgb(10, 163, 234);
  color: #f6f6f9;
  display: inline-block;
  padding: 10px 15px 10px;
  text-decoration: none;
  cursor: pointer;
  border-radius: 2rem;
  background: rgba(9, 0, 0, 0.73);
}

.button span:first-child {
  position: relative;
  transition: color 600ms cubic-bezier(0.48, 0, 0.12, 1);
  z-index: 10;
}

.button span:last-child {
  color: white;
  display: block;
  position: absolute;
  bottom: 0;
  transition: all 500ms cubic-bezier(0.48, 0, 0.12, 1);
  z-index: 100;
  opacity: 0;
  top: 65.5%;
  left: 50%;
  transform: translateY(225%) translateX(-50%);
  height: 14px;
  line-height: 13px;
}

.button:after {
  content: "";
  position: absolute;
  bottom: -50%;
  left: 0;
  width: 100%;
  height: 100%;
  background-color: rgb(60, 190, 250);
  transform-origin: bottom center;
  transition: transform 600ms cubic-bezier(0.48, 0, 0.12, 1);
  transform: skewY(9.3deg) scaleY(0);
  z-index: 50;
}

.button:hover:after {
  transform-origin: bottom center;
  transform: skewY(9.3deg) scaleY(2);
}

.button:hover span:last-child {
  transform: translateX(-50%) translateY(-100%);
  opacity: 1;
  transition: all 900ms cubic-bezier(0.48, 0, 0.12, 1);
}
</style>  