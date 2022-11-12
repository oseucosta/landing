<script lang="ts" setup>
import { ref } from "vue";

const routes = ref([
  {
    name: "Projects",
    path: "/projects",
  },
  {
    name: "Posts",
    path: "/posts",
  },
]);
</script>

<template lang="pug">
header
  nav
    ul
      li(v-for="({name, path}, index) in routes" :key="index")
        nuxt-link(:to="path") {{name}}
    div
      span [icon]
</template>

<style lang="stylus" scoped>
header
  background-color #FFFFFF

  nav
    display flex
    justify-content space-between
    align-items center

    padding 30px

    ul
      display flex
      list-style-type none

      li
        margin-left 16px

        &:nth-child(1)
          margin-left 0px
</style>
