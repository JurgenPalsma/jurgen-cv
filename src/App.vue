<template>
  <div id="app">

<div class="container"></div>
    <nav class="navbar header-top fixed-top navbar-expand-lg  navbar-dark bg-dark">
      <a class="navbar-brand" style="color:white" @click="linkTo('Home')">Jurgen Palsma</a>

      <div class="collapse navbar-collapse" id="navbarText">

        <ul class="navbar-nav ml-md-auto d-md-flex">
          <li class="nav-item">
            <a class="nav-link" @click="linkTo('Home')"> Home</a>
          </li>

          <li>
            <a class="nav-link" target="_blank" href="https://jurgenpalsma.github.io/portfolio/static/pdfs/jurgen-cv-en.pdf">CV</a>
          </li>
        </ul>
      </div>
    </nav>
    <router-view/>
    
    <div class="footer">
              <foot/>
    </div>



  </div>

</template>

<script>

import Foot from './components/Footer.vue'
import Tags from './tags.js'

export default {
  name: 'App',

  data () {
    return {
      tags: Tags
    }
  },

  methods: {
    linkTo: function(path){
      this.$router.push({name: path})
    }
  },

  components: {
    'foot': Foot
  }
}
</script>

<style scoped>
html {
  position: relative;
    min-height: 100%;
    height: 100%;
    overflow-x: hidden;
    overflow-y: scroll;
}
body {
  margin-bottom: 60px;
}
.footer {
  position: absolute;
  width: 100%;
  height: 60px;
  background-color: #f5f5f5;
}


</style>
