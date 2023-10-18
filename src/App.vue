<template>
  <div id="app">
    <div class="reveal">
      <div class="slides">
        <TitleSlide/>
        <WhatIsPihole/>
      </div>
    </div>
  </div>
</template>

<script>
import Reveal from "reveal.js";
import Markdown from "reveal.js/plugin/markdown/markdown.js";
import Highlight from "reveal.js/plugin/highlight/highlight.js";
import "reveal.js/dist/reveal.css";
import "reveal.js/dist/theme/night.css";
import "reveal.js/plugin/highlight/monokai.css";
import TitleSlide from "@/components/TitleSlide.vue";
import WhatIsPihole from "@/components/WhatIsPihole.vue";

export default {
  name: "App",
  components: {TitleSlide, WhatIsPihole},
  mounted() {
    Reveal.initialize({
      plugins: [Markdown, Highlight],
      markdown: {
        breaks: true,
        gfm: true,
      },
    });
  },
};
</script>

<style>
#app {
  font-family: "Avenir", Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
  height: 90vh;
}
</style>
