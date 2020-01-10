<template>
  <div>
    <div class="context233">
      <h1 class="title">Contact us</h1>
      <h2 class="subtitle">@moffhubsolutions</h2>
    </div>
    <div class="area233">
      <ul class="circles">
        <li/>
        <li/>
        <li/>
        <li/>
        <li/>
        <li/>
        <li/>
        <li/>
        <li/>
        <li/>
      </ul>
    </div>
    <section class="hero is-small">

      <div class="hero-body">
        <div class="columns has-text-centered">
          <div class="column">
            <i class="fa fa-twitter-square fa-3x"/>
            <h3>@moffhubsolutions</h3>
          </div>
          <div class="column">
            <i class="fa fa-facebook-square fa-3x"/>
            <h3>@moffhubsolutions</h3>
          </div>
          <div class="column">
            <i class="fa fa-instagram fa-3x"/>
            <h3>@moffhubsolutions</h3>
          </div>
        </div>
        <br/>
        <h1 class="title has-text-centered">Or Send us a message</h1>
        <div class="columns">
          <div class="column is-12-mobile is-8 is-offset-0-mobile is-offset-2">
            <div class="container">
              <form name="contact" class="contact-form" method="POST" data-netlify="true">
                <div class="field">
                  <label class="label">Name</label>
                  <div class="control">
                    <input class="input" name="name" type="text" placeholder="Your Name .."/>
                  </div>
                </div>
                <div class="field">
                  <label class="label">Email</label>
                  <div class="control">
                    <input class="input" name="email" type="email" placeholder="Your Email ..." value/>
                  </div>
                </div>
                <div class="field">
                  <label class="label">Subject</label>
                  <div class="control">
                    <div class="">
                      <select class="input" name="subject">
                        <option selected>Select Subject</option>
                        <option value="Inquiry">Inquiry</option>
                        <option value="Invoice">Request Invoice</option>
                        <option value="Meeting">Request Meeting</option>
                      </select>
                    </div>
                  </div>
                </div>

                <div class="field">
                  <label class="label">Message</label>
                  <div class="control">
                    <textarea class="textarea" name="message" placeholder="Your Messages"></textarea>
                  </div>
                </div>
                <div class="field ">
                  <div class="control">
                    <button class="button is-rounded is-medium is-success">Submit</button>
                  </div>
                </div>
              </form>
            </div>
          </div>
        </div>
      </div>
    </section>
  </div>
</template>
<script>
  export default {
    head() {
      return {
        title: "Contact Us - MoffHub Solutions",
        meta: [
          {
            hid: "description",
            name: "description",
            content:
              "You want to reach MoffHub Solutions, for any website and iot custom solutions,you can get us here "
          }
        ]
      };
    }
  };
</script>
<style scoped>
  .contact-form {
    width: 100%;
    padding: 20px;
    margin: 0 auto;
  }
  * {
    box-sizing: border-box;
  }
  input{
    width: 100%;
    height: 50px;
    border: 1px solid #ccc;
    border-radius: 25px;
    box-sizing: border-box;
    resize: vertical;
  }
  textarea {
    border-radius: 25px;
  }
  select {
    height: 50px;
    /*border-radius: 25px;*/
  }
  select option {
    margin: 40px;
    background: rgb(76, 171, 255);
    color: #fff;
    text-shadow: 0 1px 0 rgba(0, 0, 0, 0.4);
  }
  button {
    width: 100%;
  }
</style>
