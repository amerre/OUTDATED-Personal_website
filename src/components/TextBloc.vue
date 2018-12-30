<template>
  <div class="wrapper">
    <transition name="fade">
      <app-ItsMe v-if="hiddenText.itsMe"/>
    </transition>
    <img
      src="../assets/images/technologist.png"
      class="wrapper__emoji"
      @mouseover="hiddenText.itsMe = true"
      @mouseleave="hiddenText.itsMe = false"
      alt="Technologist"
    >
    <p>Hi, I’m Adrien</p>
    <p>I’m living in Montreuil, near Paris, where I’m studying in
      <app-Link linkText="Hetic" :linkUrl="HeticLink"/>. I’m playing around with web development, design and project management.
    </p>
    <p>I’m actualy a front-end developer, but currently learning Vue.js and Node.js in order to become a full-stack Javascript ninja.</p>
    <p>To see some of my work, check my
      <app-Link linkText="Github" :linkUrl="GithubLink"/>&nbsp;or my
      <app-Link linkText="Codepen" :linkUrl="CodepenLink"/>.
    </p>
    <p>
      I’m open to any work propositions, but I’m looking especially for an 5-month internship in June 2019, feel free to
      <span
        @mouseover="hiddenText.wontRegret = true"
        @mouseleave="hiddenText.wontRegret = false"
      >
        <app-Link linkText="drop me a line" :linkUrl="EmailLink"/>
      </span>.
      <transition name="fade">
        <appWontRegret v-if="hiddenText.wontRegret"/>
      </transition>
    </p>
  </div>
</template>

<script>
import Link from "../components/UnderlinedLinks.vue";
import ItsMe from "../components/HiddenText/ItsMe.vue";
import YouWontRegret from "../components/HiddenText/YouWontRegret.vue";

export default {
  components: {
    appLink: Link,
    appItsMe: ItsMe,
    appWontRegret: YouWontRegret
  },
  data() {
    return {
      // Is hidden text displayed ?
      hiddenText: {
        itsMe: false,
        wontRegret: false
      }
    };
  },
  // Links imported from App.vue
  props: {
    HeticLink: String,
    GithubLink: String,
    CodepenLink: String,
    EmailLink: String
  }
};
</script>

<style scoped lang="scss">
@import "../assets/scss/_variables.scss";
.wrapper {
  // 220 - mtop = 150 / 170 - mtop = 100 / 120 - mtop = 50
  min-height: calc(100vh - 220px);
  line-height: 27px;
  .wrapper__emoji {
    cursor: pointer;
    height: 60px;
  }
  p {
    font-size: 20px;
    color: $first-color;
  }
  .wrapper__underline {
    background-color: $second-color;
    text-decoration: none;
    color: $first-color;
  }
}
.fade-enter-active,
.fade-leave-active {
  transition: opacity 0.5s;
}
.fade-enter,
.fade-leave-to {
  opacity: 0;
}
@import "../assets/scss/_responsive.scss";
</style>
