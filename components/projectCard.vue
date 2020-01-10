<template>
  <div class="card">
    <div class="card-image">
      <figure class="image is-4by3">
        <img
          :src="image"
          alt="Placeholder image"
        />
      </figure>
    </div>
    <div class="card-content">
      <div class="media">
        <div class="media-content">
          <a :href="url" target="_blank" class="title is-4">{{title}}</a>
          <p class="subtitle is-6">@{{subtitle}}</p>
        </div>
      </div>

      <div class="content">
        {{content}}
        <br/>
      </div>
      <hr class="hr">
      <time>{{tags}}</time>
    </div>
  </div>
</template>

<script>
  export default {
    name: "projectCard",
    props: [
      "image",
      "title",
      "subtitle",
      "content",
      "tags",
      "url"
    ]
  }
</script>

<style scoped>
  hr {
    height: 5px;
  }

  p,a {
    align-content: center;
    margin: 16px;
  }

  /*a {*/
  /*  margin: 16px;*/
  /*}*/

  .card {
    /*background-color: rgb(89, 102, 216);*/
    border-bottom-right-radius: 5%;
    border-top-left-radius: 5%;
    color: #060606;
    background: #cbe2c1;
    background: -webkit-linear-gradient(to right, #adcfd3, #edfffd);
    background: -moz-linear-gradient(to right, #adcfd3, #edfffd);
    background: linear-gradient(to right, #adcfd3, #edfffd);
    text-align: left;

  }

  .card:hover {
    box-shadow: 2px 2px #ff0016;
  }

  .card-image {
    border-top-left-radius: 5%;
    border-bottom-right-radius: 5%;
    overflow: hidden;
  }

  .content {
    text-align: left;
    font-size: 17px;
    font-weight: bolder;
  }

  .card img {
    -webkit-transition: all .4s ease-in-out;
    -moz-transition: all .4s ease-in-out;
    -o-transition: all .4s ease-in-out;
    -ms-transition: all .4s ease-in-out;
  }

  .card .title {
    color: red;
    text-align: left;
    margin: 15px;
  }

  .card .subtitle {
    color: blue;
    margin: 15px;
  }

  .card img:hover {
    transform: scale(1.15);
  }
</style>
