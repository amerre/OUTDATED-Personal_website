<template>
  <div class="wrapper">
    <transition name="fade">
      <app-ItsMe v-if="hiddenText.itsMe"/>
    </transition>
    <span
      class="wrapper__emoji"
      @mouseover="hiddenText.itsMe = true"
      @mouseleave="hiddenText.itsMe = false"
    >👨🏻‍💻</span>
    <p>Hi, I’m Adrien</p>
    <p>I’m living in Montreuil, near Paris, where I’m studying in
      <app-Link linkText="Hetic" :linkUrl="hetic"/>. I’m playing around with web development, design and project management.
    </p>
    <p>I’m actualy a front-end developer, but currently learning Vue.js and Node.js in order to become a full-stack Javascript ninja.</p>
    <p>To see some of my work, check my
      <app-Link linkText="Github" :linkUrl="github"/>&nbsp;or my
      <app-Link linkText="Codepen" :linkUrl="codepen"/>.
    </p>
    <p>
      I’m open to any work propositions, but I’m looking especially for an 5-month internship in June 2019, feel free to
      <span
        @mouseover="hiddenText.wontRegret = true"
        @mouseleave="hiddenText.wontRegret = false"
      >
        <app-Link linkText="drop me a line" :linkUrl="email"/>
      </span>.
      <transition name="fade">
        <appWontRegret v-if="hiddenText.wontRegret"/>
      </transition>
    </p>
  </div>
</template>

<script>
import Link from "../components/Link.vue";
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
      hetic: "https://www.hetic.net/formations/grande-ecole",
      github: "https://github.com/amerre",
      codepen: "https://codepen.io/adrizu/",
      email: "mailto:adr.merre@gmail.com",
      hiddenText: {
        itsMe: false,
        wontRegret: false
      }
    };
  }
};
</script>

<style scoped lang="scss">
@import "../scss/_variables.scss";
.wrapper {
  min-height: calc(100vh - 170px);
  line-height: 27px;
  .wrapper__emoji {
    font-size: 55px;
    cursor: pointer;
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
</style>
