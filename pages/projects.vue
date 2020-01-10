<template>
  <div>
    <div class="context233">
      <h1 class="title">Our Projects</h1>
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
        <div class="container is-fluid has-text-centered">
          <h1 class="title">Our Web Projects</h1>
          <hr>
          <div class="columns is-multiline">
            <div class="column is-one-quarter" v-for="(project,i) in webProjects" :key="i">
              <project-card :image="project.image" :title="project.title" :subtitle="project.subtitle"
                            :content="project.content" :tags="project.tags" :url="project.url"/>
            </div>
          </div>
          <br/>
          <h1 class="title">IoT Projects</h1>
          <hr>
          <div class="columns is-multiline">
            <div class="column is-one-quarter" v-for="(project,i) in iotProjects" :key="i">
              <project-card :image="project.image" :title="project.title" :subtitle="project.subtitle"
                            :content="project.content" :tags="project.tags" :url="project.url"/>
            </div>
          </div>
          <h1 class="title">Mobile App Projects</h1>
          <hr>
          <h1 class="title">Archived Projects</h1>
          <hr/>

        </div>
      </div>
    </section>
  </div>
</template>
<style scoped>

</style>
<script>
  import projectCard from "../components/projectCard";

  export default {
    components: {
      projectCard
    },
    data() {
      return {
        webProjects: [
          {
            title: "E-Matatu",
            subtitle: "ematatu",
            image: "/imgs/Ematatu.png",
            content: "A Matatu cashless payment system that integrates mobile money, accounting, record keeping and real-time analysis.",
            tags: "Laravel, Vue js, Mpesa",
            url: "https://www.ematatu.co.ke"
          },
          {
            title: "CFL",
            subtitle: "cfl",
            image: "/imgs/CFL.png",
            content: "A fuel management system for Central fuels and Lubricants ltd",
            tags: "Laravel, Vue js, Mpesa",
            url: "https://www.cfl-lamu.co.ke"
          },
          {
            title: "Viakwetu",
            subtitle: "viakwetu",
            image: "/imgs/Viakwetu.png",
            content: "A healthy and Organic Food website for growing herbs, spices both nutritional and medicinal.",
            tags: "Laravel, Vue js, Mpesa,Ecommerce",
            url: "https://www.ematatu.co.ke"
          },
          {
            title: "Nashcom Ltd",
            subtitle: "nashcom",
            image: "/imgs/Nashcom.png",
            content: "A network company website that showcases the unique features and services of Nashcom solutions.",
            tags: "Laravel",
            url: "https://www.ematatu.co.ke"
          },
          {
            title: "Mandera County Revenue System",
            subtitle: "manderarcms",
            image: "/imgs/Nashcom.png",
            content: "An integrated web app for collecting funds,integration to MPesa, and use of USSD.",
            tags: "Vue Js, Laravel,USSD,Mpesa",
            url: "https://www.ematatu.co.ke"
          },
          {
            title: "Anzia Sokoni",
            subtitle: "anziasokoni",
            image: "/imgs/AnziaSokoni.png",
            content: "A movement of modern farmers who appreciate the need to do market-driven agriculture.",
            tags: "Vue Js, Laravel,Mpesa",
            url: "http://anziasokoni.com"
          },
          {
            title: "HTorex",
            subtitle: "htorex",
            image: "/imgs/Htorex.jpeg",
            content: "A 6 in 1 tourism integrated portal that allows easy exchange of tourism products across the globe.",
            tags: "Vue Js, Laravel,Mpesa",
            url: "http://anziasokoni.com"
          },
        ],
        iotProjects: [
          {
            title: "HewaSense",
            subtitle: "hewasense",
            image: "/imgs/layout1.png",
            content: "A smart way to determine the air quality, gas and dust levels in modern urban centres in large IoT network.",
            tags: "Arduino, Sensors, LoRa",
            url: ""
          },
          {
            title: "TeleBoards",
            subtitle: "teleboards",
            image: "/imgs/layout2.png",
            content: "A series ot IOT boards for TeleOps.io.",
            tags: "Arduino, Sensors, LoRa",
            url: ""
          },
        ]
      }
    },
    head() {
      return {
        title: "Our Projects - MoffHub Solutions",
        meta: [
          {
            hid: "description",
            name: "description",
            content:
              "These are sample works and services at Moffhub Solutions. We are good at what we do "
          }
        ]
      };
    }
  };
</script>
<style scoped>
  .columns > div > div.card {
    height: calc(100% - 15px);
    margin-bottom: 15px;
  }
</style>
