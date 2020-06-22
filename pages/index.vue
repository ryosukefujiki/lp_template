<template>
  <div class="container">
    <div>
      <logo />
      <h1 class="title">
        lp_template
      </h1>
      <h2 class="subtitle">
        LP_Template Page
      </h2>
      <div class="links">
        <a
          href="https://nuxtjs.org/"
          target="_blank"
          class="button--green"
        >
          Documentation
        </a>
        <a
          href="https://github.com/nuxt/nuxt.js"
          target="_blank"
          class="button--grey"
        >
          GitHub
        </a>
      </div>
    </div>
  </div>
</template>

<script lang="ts">
import Vue from 'vue'
import Logo from '~/components/Logo.vue'

import { mapGetters } from "vuex";
import { TweenMax, Elastic, Expo, Back, Linear } from "gsap";

export default Vue.extend({
  components: {
    Logo
  },
  data() {
    return {
    }
  },
  methods: {
    testMethod: function() {
    },
  },
  computed: {
    ...mapGetters({
      leftMove: "leftClicked"
    })
  },
  watch: {
   async leftMove(val) {
    //  requestAnimationFrame(() => {
    //     TweenMax.to("", 0.1, {
    //       opacity: 1,
    //       ease: Expo.easeIn,
    //       onComplete: function() {
    //       }
    //     });
    //     TweenMax.staggerTo(
    //       ".TheDetail_Greeting_Header",
    //       0.2,
    //       {
    //         delay: 0.1,
    //         ease: Expo.easeIn,
    //         opacity: 1
    //       },
    //       0.2
    //     );
    //   });
    //  await this.$delay(500);
    //  this.$router.push("/detail");
   }
  },
  mounted() {
    // window.addEventListener("scroll", this.scrollStart, false);
  },
  destroyed() {
    // window.removeEventListener("scroll", this.scrollStart, false);
  }
})
</script>

<style>
.container {
  margin: 0 auto;
  min-height: 100vh;
  display: flex;
  justify-content: center;
  align-items: center;
  text-align: center;
}

.title {
  font-family: 'Quicksand', 'Source Sans Pro', -apple-system, BlinkMacSystemFont,
    'Segoe UI', Roboto, 'Helvetica Neue', Arial, sans-serif;
  display: block;
  font-weight: 300;
  font-size: 100px;
  color: #35495e;
  letter-spacing: 1px;
}

.subtitle {
  font-weight: 300;
  font-size: 42px;
  color: #526488;
  word-spacing: 5px;
  padding-bottom: 15px;
}

.links {
  padding-top: 15px;
}

@media screen and (max-width: 1024px) {
}
@media screen and (max-width: 768px) {
}
@media screen and (max-width: 480px) {
}
@media screen and (max-width: 320px) {
}
</style>
