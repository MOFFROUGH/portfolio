<template>
  <div class="about has-text-left">
    <div class="tile is-parent has-text-centered">
      <article class="tile is-child notification">
        <p class="title">Portfolio</p>
        <p>We are pushing the SMEs to the next level in the following fields</p>
        <hr>
        <p class="subtitle">Financial Technology Solutions</p>
        <p class="subtitle">Internet of things (IOT) Solutions</p>
        <p class="subtitle">Transport and Transit Solutions</p>
        <p class="subtitle">School and Education Solutions</p>
        <p class="subtitle">Hotel and Tourism Solutions</p>
        <p class="subtitle">Fuel and Energy Solutions</p>
        <p class="subtitle">Agricultural Solutions</p>
        <p class="subtitle">E-Commerce Solutions</p>
        <p class="subtitle">Consultancy</p>
        <div class="content">
          <!-- Content -->
        </div>
      </article>
    </div>
    <div class="tile is-ancestor">
      <div class="tile is-vertical is-8">
        <div class="tile">
          <div class="tile is-parent is-vertical">
            <article class="tile is-child notification">
              <p class="title">Website UI/UX</p>
              <hr>
              <p class="subtitle">HTML5</p>
              <p class="subtitle">CSS3</p>
              <p class="subtitle">JavaScript</p>
              <p class="subtitle">Vue Js</p>
              <p class="subtitle">Bootstrap</p>
              <p class="subtitle">Material Design</p>
              <p class="subtitle">Bulma</p>
            </article>
            <article class="tile is-child notification">
              <p class="title">Website Backend</p>
              <hr>
              <p class="subtitle">Node JS</p>
              <p class="subtitle">Express JS</p>
              <p class="subtitle">PHP</p>
              <p class="subtitle">Laravel</p>
              <p class="subtitle">Python</p>
            </article>
          </div>
          <div class="tile is-parent">
            <article class="tile is-child notification">
              <p class="title">Database Design</p>
              <hr>
              <p class="subtitle">MySQL</p>
              <p class="subtitle">SQLite</p>
              <p class="subtitle">PostgresSQL</p>
              <p class="subtitle">Firebase</p>
              <p class="subtitle">MongoDB</p>
              <p class="subtitle">Graph Concepts</p>
            </article>
          </div>
        </div>
        <div class="tile is-parent">
          <article class="tile is-child notification">
            <p class="title">IOT</p>
            <hr>
            <p class="subtitle">Arduino based controllers</p>
            <p class="subtitle">Raspberry Pi MVP</p>
            <p class="subtitle">PLC system design</p>
            <p class="subtitle">LoRa wireless technology</p>
            <p class="subtitle">Zigbee wireless technology</p>
            <p class="subtitle">Bluetooth, NFC, RFID systems</p>
            <p class="subtitle">GSM, LTE,SMS based systems</p>
            <div class="content">
              <!-- Content -->
            </div>
          </article>
        </div>
      </div>
      <div class="tile is-parent">
        <article class="tile is-child notification">
          <div class="content">
            <p class="title">Other Services</p>
            <hr>
            <p class="subtitle">Mobile App development.</p>
            <p class="subtitle">Search Engine Optimization SEO</p>
            <p class="subtitle">System upgrade and Maintenance</p>
            <p class="subtitle">Mpesa Integration</p>
            <p class="subtitle">Bulk SMS integration</p>
            <p class="subtitle">USSD App development.</p>
            <p class="subtitle">API development</p>
            <p class="subtitle">Custom Application development</p>
            <p class="subtitle">Custom Plugins development</p>
            <p class="subtitle">Custom PCB development</p>
            <div class="content">
              <!-- Content -->
            </div>
          </div>
        </article>
      </div>
    </div>
  </div>
</template>

<script>
  export default {
    name: "serviceComponent"
  }
</script>

<style scoped>
.about {
  margin: 10px;
}
  .tile .is-child{
    background-color: #3B8070;
    color: white;
  }
</style>
