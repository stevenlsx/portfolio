<template>

  <router-view v-slot="{ Component, route }">
    <transition :name="route.meta.transition" mode="out-in">
      <component :is="Component" />
    </transition>
  </router-view>
</template>

<script>
</script>
<style lang="scss">
@import "assets/scss/animMixin.scss";

* {
  margin: 0;
  padding: 0;
  height: 100%;
}

@font-face {
  font-family: "raleway";
  src: local("fonts"),
    url(./fonts/Raleway-Regular.ttf) format("truetype");
  font-family: "ralewayB";
  src: local("fonts"),
    url(./fonts/Raleway-Bold.ttf) format("truetype");
}


.slide-up-enter-active {
  @include slide-up-project;
  animation: slide-up-project 0.7s ease-in-out;
}


.slide-up-leave-active {
  @include slide-up-accueil;
  animation: slide-up-accueil 1s ease-in-out;
}
</style>
