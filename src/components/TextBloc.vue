<template>
  <div class="wrapper">
    <transition name="fade">
      <app-ItsMe v-if="hiddenText.itsMe" />
    </transition>
    <img
      src="../assets/images/technologist.png"
      class="wrapper__emoji"
      @mouseover="hiddenText.itsMe = true"
      @mouseleave="hiddenText.itsMe = false"
      alt="Technologist"
    />
    <p>Hey, moi c'est Adrien</p>
    <p>Je vis dans la Manche, en Normandie. Mon truc c'est l'informatique et la création de contenus audiovisuels.</p>
    <p>
      Je suis à la recherche d'une alternance pour septembre 2020, mais je suis également ouvert à tout type de proposition. N'hesitez donc pas à m'envoyer un
      <span
        @mouseover="hiddenText.wontRegret = true"
        @mouseleave="hiddenText.wontRegret = false"
      >
        <app-Link linkText="mail" :linkUrl="EmailLink" />
      </span>.
      <transition name="fade">
        <appWontRegret v-if="hiddenText.wontRegret" />
      </transition>
    </p>
    <p>
      Voici quelques uns de mes projets, pour en voir plus, passez par
      <app-Link linkText="Github" :linkUrl="GithubLink" />&nbsp;ou
      <app-Link linkText="Codepen" :linkUrl="CodepenLink" />
    </p>
    <p class="projects">
      Web :
      <br />
      <app-Link linkText="Css-helper" :linkUrl="test" />&nbsp;: Un outil pour visualiser du CSS
      <br />
      <app-Link linkText="Todo-app" :linkUrl="test" />&nbsp;: Une Todo App
      <br />
      <app-Link linkText="Cosmopolitan" :linkUrl="test" />&nbsp;: Une refonte de la page d'accueil de Cosmopolitan
      <br />
      <app-Link linkText="Ikao" :linkUrl="test" />&nbsp;: Une page d'accueil d'un e-commerce fictif
      <br />
      <app-Link linkText="Newsletter" :linkUrl="test" />&nbsp;: Une newsletter fictive
    </p>
    <p class="projects">
      Audiovisuel :
      <br />
      <app-Link linkText="Portrait" :linkUrl="test" />&nbsp;: Portrait d'un facteur d'orgue
      <br />
      <app-Link linkText="Interview" :linkUrl="test" />&nbsp;: Interview d'un photographe engagé
      <br />
      <app-Link linkText="Interview" :linkUrl="test" />&nbsp;: Interview de visiteurs du Louvre Lens
      <br />
      <app-Link linkText="Reportage" :linkUrl="test" />&nbsp;: Reportage pour la FDSEA
      <br />
      <app-Link linkText="Portrait" :linkUrl="test" />&nbsp;: Portrait d'un maître tapissier
      <br />
    </p>
  </div>
</template>

<script>
import Link from "../components/UnderlinedLinks.vue";
import ItsMe from "../components/HiddenText/ItsMe.vue";

export default {
  components: {
    appLink: Link,
    appItsMe: ItsMe
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
