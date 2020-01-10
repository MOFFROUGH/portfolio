<template>
  <div>
    <div class="container">
      <div id="flow">
        <span class="flow-1"></span>
        <span class="flow-2"></span>
      </div>
      <div class="section">
        <div class="d has-text-centered">
          <h1 class="title">Our Blog</h1>
          <h2 class="subtitle">@moffhubsolutions</h2>
        </div>
        <div class="row columns is-multiline">
          <div class="column is-4" v-for="(post,i) in posts" :key="i" @click="ShowBlog(post)">
            <div class="card large">
              <div class="card-image">
                <!--                <figure class="image">-->
                <!--                  <img-->
                <!--                    :src="post.thumbnail"-->
                <!--                    alt="Image">-->
                <!--                </figure>-->
              </div>
              <div class="card-content">
                <div class="media">
                  <div class="media-content">
                    <p><span class="title is-6">
                      <a href="http://twitter.com/#">{{post.title}}</a>
                    </span></p>
                  </div>
                </div>
                <div class="content" v-html="truncate(post.content,90)">
                </div>
              </div>
            </div>
          </div>
        </div>
        <!-- End Developers -->
      </div>
    </div>
    <div class="modal" id="modal">
      <div class="modal-background"></div>
      <div class="modal-card">
        <header class="modal-card-head">
          <p class="title">{{currentpost.title}}</p>
          <button class="delete" @click="hideBlog" aria-label="close"/>
        </header>
        <section class="modal-card-body">
          <div class="" v-html="currentpost.description"></div>
        </section>
        <footer class="modal-card-foot">
          <button class="button" @click="hideBlog">Cancel</button>
        </footer>
      </div>
    </div>
  </div>
</template>
<script>
  import axios from "axios";
  // import ShareTo from '../components/ShareTo.vue'
  export default {
    components: {
      //   ShareTo
    },
    data() {
      return {
        posts: [],
        postsav: false,
        currentpost: []
      };
    },
    created() {
      this.getPosts();
    },
    methods: {
      ShowBlog(post) {
        this.currentpost = post;
        var modal = document.getElementById("modal");
        modal.classList.add("is-active");
      },
      hideBlog() {
        this.currentpost = [];
        var modal = document.getElementById("modal");
        modal.classList.remove("is-active");
      },
      truncate(str, no_words) {
        return str
          .split(" ")
          .splice(0, no_words)
          .join(" ");
      },
      getPosts() {
        var data = "?rss_url=https://medium.com/feed/@moffhubsolutions";
        var self = this;
        axios
          .get(
            "https://api.rss2json.com/v1/api.json?rss_url=https://medium.com/feed/@moffhubsolutions"
          )
          .then(function (response) {
            // handle success
            const feed = response.data.items;
            self.posts = feed;
            if (feed.length > 0) {
              self.postsav = true;
            }
            // console.log(self.posts);
          })
          .catch(function (error) {
            // handle error
            console.warn(error);
          });
      }
    }
  };
</script>
<style scoped>
  body {
    background: #041221;
  }

  .d {
    margin-top: 100px;
    margin-bottom: 30px;
    color: red;
  }

  /* Card start*/
  .card {
    overflow: hidden
  }

  .card.large {
    height: 600px;
    -webkit-backface-visibility: hidden;
    backface-visibility: initial;
    border-radius: 5px;
  }

  .card-content {
    margin-top: 30px;
  }

  /* Card end */
  .media-content {
    margin: 10px;
    overflow: hidden;
  }

  .title.no-padding {
    margin-bottom: 0 !important;
  }

  #flow span {
    display: block;
    width: 200vw;
    height: 200vw;
    position: absolute;
    top: -180vw;
    left: -50vw;
    border-radius: 90vw;
    opacity: .4;
  }

  .flow-1 {
    background: #ff4f5a;
    -webkit-animation: rotating 20s linear infinite;
    -moz-animation: rotating 20s linear infinite;
    -ms-animation: rotating 20s linear infinite;
    -o-animation: rotating 20s linear infinite;
    animation: rotating 20s linear infinite;
  }

  .flow-2 {
    background: #30f45d;
    position: absolute;
    -webkit-animation: rotating 15s linear infinite;
    -moz-animation: rotating 15s linear infinite;
    -ms-animation: rotating 15s linear infinite;
    -o-animation: rotating 15s linear infinite;
    animation: rotating 15s linear infinite;
  }

  @-webkit-keyframes rotating {
    from {
      -ms-transform: rotate(0deg);
      -moz-transform: rotate(0deg);
      -webkit-transform: rotate(0deg);
      -o-transform: rotate(0deg);
      transform: rotate(0deg);
    }
    to {
      -ms-transform: rotate(360deg);
      -moz-transform: rotate(360deg);
      -webkit-transform: rotate(360deg);
      -o-transform: rotate(360deg);
      transform: rotate(360deg);
    }
  }

  @keyframes rotating {
    from {
      -ms-transform: rotate(0deg);
      -moz-transform: rotate(0deg);
      -webkit-transform: rotate(0deg);
      -o-transform: rotate(0deg);
      transform: rotate(0deg);
    }
    to {
      -ms-transform: rotate(360deg);
      -moz-transform: rotate(360deg);
      -webkit-transform: rotate(360deg);
      -o-transform: rotate(360deg);
      transform: rotate(360deg);
    }
  }

  .rotating {
    -webkit-animation: rotating 2s linear infinite;
    -moz-animation: rotating 2s linear infinite;
    -ms-animation: rotating 2s linear infinite;
    -o-animation: rotating 2s linear infinite;
    animation: rotating 2s linear infinite;
  }

  .footer {
    background-color: #222831;
    color: lemonchiffon;
  }

  .footer p, strong {
    color: lemonchiffon
  }

  .footer a:hover {
    color: crimson;
  }

</style>
