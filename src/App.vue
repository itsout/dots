<template>
  <div id="app">
    <transition name='slide-fade'>
      <router-view/>
    </transition>
  </div>
</template>

<script>
export default {
  name: 'App'
}
</script>

<style lang="scss">
// @import url('https://fonts.googleapis.com/css2?family=Ubuntu:wght@300;400&display=swap');

#app {
  font-family: 'Ubuntu', sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  min-height: 100vh;
  background: linear-gradient(270deg, #ff9a9e, #fad0c4, #fbc2eb, #a1c4fd, #c2e9fb, #d4fc79, #96e6a1, #fbc2eb, #ff9a9e);
  background-size: 1800% 1800%;
  animation: gradientBG 24s ease infinite;
}

@keyframes gradientBG {
  0% {background-position: 0% 50%;}
  50% {background-position: 100% 50%;}
  100% {background-position: 0% 50%;}
}

@media screen and (max-width: 960px) {
  .container {
    padding: 0 5%
  }
}

@media screen and (min-width: 900px) {
  .container {
    max-width: 900px
  }
}

// Import Bulma's core
@import "bulma/sass/utilities/_all";

// Set your colors
$primary: #8c67ef;
$primary-invert: findColorInvert($primary);
$twitter: #4099FF;
$twitter-invert: findColorInvert($twitter);

// Setup $colors to use as bulma classes (e.g. 'is-twitter')
$colors: (
    "white": ($white, $black),
    "black": ($black, $white),
    "light": ($light, $light-invert),
    "dark": ($dark, $dark-invert),
    "primary": ($primary, $primary-invert),
    "info": ($info, $info-invert),
    "success": ($success, $success-invert),
    "warning": ($warning, $warning-invert),
    "danger": ($danger, $danger-invert),
    "twitter": ($twitter, $twitter-invert)
);

// Links
$link: $primary;
$link-invert: $primary-invert;
$link-focus-border: $primary;

// For buefy
$speed-slow: 150ms !default;
$speed-slower: 250ms !default;

// Import Bulma and Buefy styles
@import "bulma/bulma";
@import "buefy/src/scss/utils/_animations.scss";
@import "buefy/src/scss/components/_notices.scss";

@import "buefy/src/scss/utils/_functions.scss";

.slide-fade-enter-active {
  transition: all .3s ease;
}
.slide-fade-leave-active {
  transition: all .2s cubic-bezier(1.0, 0.5, 0.8, 1.0);
}
.slide-fade-enter, .slide-fade-leave-to {
  transform: translateX(10px);
  opacity: 0;
  position: absolute;
  left: 0;
  right: 0;
}
</style>
