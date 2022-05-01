<template>
  <div
    class="w-full min-h-screen flex justify-center transition-all flex-col items-center px-4"
    :class="imgLoaded ? 'opacity-100' : 'opacity-0'"
  >
    <div class="w-full"></div>

    <img
      src="@/assets/img/AAAAA.png"
      @load="onImgLoad"
      class="w-full h-full max-w-5xl"
      alt=""
    />

    <nuxt-link
      v-show="load"
      to="/NasProgram"
      class="headline text-sm md:text-xl transition-opacity hover:opacity-50"
    >
      Náš program</nuxt-link
    >
  </div>
</template>

<script>
export default {
  name: 'IndexPage',
  transition: 'home',
  data() {
    return {
      imgLoaded: false,
    }
  },

  computed: {
    load() {
      return this.imgLoaded
    },
  },

  methods: {
    onImgLoad() {
      console.log('loaded')

      this.imgLoaded = true
    },
  },
}
</script>

<style lang="scss">
body {
  overflow-x: hidden;
}

.headline {
  font-family: 'headline', serif;
}
.home-enter-active,
.home-leave-active {
  transition: opacity 0.5s;
}
.home-enter,
.home-leave-active {
  opacity: 0;
}
</style>
