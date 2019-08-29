<template>
  <div>
    <h1 class="title has-text-centered">Our Blog</h1>
    <section class="section">
      <div class="container">
        <!-- FIRST ROW -->
        <div class="tile is-ancestor" v-for="(post,i) in posts" :key="i">
          <div class="tile is-parent">
            <article class="tile is-child green post">
              <h2 class="post__title">{{post.title}}</h2>
              <div class="post__content" v-html="truncate(post.content,50)"></div>
              <a class @click="ShowBlog(post)">Read more</a>
              <br />
            </article>
          </div>
        </div>
        <div v-if="!postsav">
          <h2 class="subtitle">No Blogs Yet</h2>
        </div>
      </div>
      <!-- /container -->
    </section>
    <div class="modal" id="modal">
      <div class="modal-background"></div>
      <div class="modal-card">
        <header class="modal-card-head">
          <p class="modal-card-title">{{currentpost.title}}</p>
          <button class="delete" aria-label="close" @click="hideBlog()"></button>
        </header>
        <section class="modal-card-body">
          <div v-html="currentpost.content"></div>
          <!-- <share-to></share-to> -->
        </section>
        <footer class="modal-card-foot">
          <a :href="currentpost.guid" class="btn is-success" target="_blank">View on Medium</a>
          <button class="button" @click="hideBlog()">Close</button>
        </footer>
      </div>
    </div>
  </div>
</template>
<script>
import axios from "axios";
// import ShareTo from '../components/ShareTo.vue'
export default {
  components:{
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
        .then(function(response) {
          // handle success
          const feed = response.data.items;
          self.posts = feed;
          if (feed.length > 0) {
            self.postsav = true;
          }
          console.log(self.posts);
        })
        .catch(function(error) {
          // handle error
          console.warn(error);
        });
    }
  }
};
</script>
<style lang="css" scoped>
.btn {
  margin: 12px;
  background-color: rgb(187, 199, 186);
  padding: 5px;
  border-radius: 5%;
  text-transform: uppercase;
}
.post {
  position: relative;
  padding: 20px;
  flex-basis: auto;
}

.post__category {
  font-size: 0.8rem;
  text-transform: uppercase;
}

.post__title {
  font-size: 1.8rem;
  font-weight: 600;
  margin: 20px 0 10px;
}

.post__content {
  font-size: 1.3rem;
  margin-bottom: 50px;
}

.post__category,
.post__permalink {
  color: #4a4a4a;
  text-decoration: underline;
}

.post__permalink {
  position: absolute;
  bottom: 20px;
}

.fb-auto {
  flex-basis: auto;
}

.pink {
  background: #ffdae0;
}

.gray {
  background: #e7f0da;
}

.green {
  background: #ddebd0;
}

.gold {
  background: #fcf5b6;
}

.blue {
  background: #cae9ef;
}

.red {
  background: #f8c9c1;
}
</style>