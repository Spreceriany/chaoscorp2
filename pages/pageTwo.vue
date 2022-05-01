<template>
  <div>
    <p>hey</p>
  </div>
</template>

<script>
export default {
  name: 'pageTwo',
  transition: 'home',
}
</script>

<style lang="scss" scoped>
.home-enter-active,
.home-leave-active {
  transition: opacity 0.5s;
}
.home-enter,
.home-leave-active {
  opacity: 0;
}
</style>
