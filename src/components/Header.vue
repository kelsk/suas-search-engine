<template>
  <header>
    <div>
      <h1>
        <a href="/">
        Shut Up & Sew search engine
        </a>
      </h1>
      <h2>
        Search all the vetted websites from <a v-bind:href="links.pinkmimosabyjacinta.url" v-bind:alt="links.pinkmimosabyjacinta.alt">
        @pinkmimosabyjacinta</a>'s 
        <a v-bind:href="links.spreadsheet.url" v-bind:alt="links.spreadsheet.alt">
        Shut Up & Sew vendor list
        </a>
      </h2>
    </div>
    <div>
      <button v-on:click="toggleAbout" class="about-btn mdc-button mdc-button--raised" id="about">
        <span class="mdc-button__label">
        About
        </span>
        </button>
    </div>
    <div v-if="!aboutHidden" v-on:click="toggleAbout" class="about-wrapper">
    </div>
      <About v-if="!aboutHidden"></About>
</header>
</template>

<script>
import About from './About.vue'

export default {
  name: 'Header',
  components: {
    About,
  },
  data: function () {
    return {
      aboutHidden: true,
      links: {
        pinkmimosabyjacinta: {
          url: process.env.VUE_APP_PMBJ_IG,
          alt: "pinkmimosabyjacinta instagram"
        },
        spreadsheet: {
          url: process.env.VUE_APP_SUAS_SPREADSHEET,
          alt: "shut up and sew spreadsheet"
        }
      }
    }
  },
  methods: {
    toggleAbout: function () {
      this.aboutHidden = !this.aboutHidden;
    }
  }
}
</script>