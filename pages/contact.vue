<template>
  <section class="hero is-success is-large">
    <div class="hero-body">
    <div class="container has-text-centered">
      <h1 class="title">Contact Me</h1>
      <p>
        You can follow me on Twitter:
        <a href="https://twitter.com/moffmu" target="_blank">@moffmu</a>
      </p>
      <p>
        You can follow me on Facebook:
        <a href="https://www.facebook.com/mofaya.visrad" target="_blank">Mofaya Moffat Munene</a>
      </p>
      <p>
        You can follow me on Instagram:
        <a href="https://www.instagram.com/moff4g/" target="_blank">@moff4g</a>
      </p>
    </div>
    <br />
    <h1 class="subtitle has-text-centered">Or Send Me a message</h1>
    <div class="columns">
      <div class="column is-half is-offset-one-quarter">
        <div class="container">
          <form name="contact" method="POST" data-netlify="true">
            <div class="field">
              <label class="label">Name</label>
              <div class="control has-icons-left">
                <input class="input" name="name" type="text" placeholder="Your Name .." />
                <span class="icon is-small is-left">
                  <i class="fa fa-user"></i>
                </span>
              </div>
            </div>

            <div class="field">
              <label class="label">Email</label>
              <div class="control has-icons-left has-icons-right">
                <input class="input" name="email" type="email" placeholder="Your Email ..." value />
                <span class="icon is-small is-left">
                  <i class="fa fa-envelope"></i>
                </span>
              </div>
            </div>

            <div class="field">
              <label class="label">Subject</label>
              <div class="control">
                <div class="select">
                  <select name="subject">
                    <option selected>Select Subject</option>
                    <option value="Invoice">Request Invoice</option>
                    <option value="Meeting">Request Meeting</option>
                    <option value="HireMe">Request To Hire Me</option>
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
            <div class="field is-grouped">
              <div class="control">
                <button class="button is-link">Submit</button>
              </div>
            </div>
          </form>
        </div>
      </div>
    </div>
    </div>
  </section>
</template>
