<template>
    <div class="contact" id="contact">
        <div class="container">
        <div class="row">
              <h2>Contact Us</h2>
            <div class="col-md-6">
              <div class="detail">
                <p class="contact-detail"><strong><i class="bi bi-envelope"></i>:</strong>  masoodbasardien123@gmail.com </p>
                <p class="contact-detail"><strong><i class="bi bi-telephone-fill"></i>:</strong> 079 298 0631 </p>
                <p class="contact-detail"><strong><i class="bi bi-geo-alt"></i>:</strong> 14 Chapel Road, Cape Town, 7785 </p>
              </div>
            </div>
            <!--  -->
            <div class="col-md-6">
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
.contact{
  padding-top: 5rem;
}  
h2{
  padding-bottom: 2rem;
}     

.col{
  border: 1px solid red;
}
.detail{
  color: black;
  font-size: 1.5rem;
}
.contact-detail{
  padding-top: 2rem;
}
@media (max-width: 991.5px) {
  .contact-detail{
    color:rgb(90, 90, 105);
    font-size: 1.2rem;
  }
}
</style>  