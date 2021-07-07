<template>
  <transition name="fade">
    <AsideBar v-show="show" :asideHandler="asideHandler"/>
  </transition>
  <Header :asideHandler="asideHandler"/>
  <h2>Hi! 快速使用vue3做出網頁template</h2>
</template>

<script>
import Header from '../components/header'
import AsideBar from '../components/asideBar'
import { ref } from '@vue/reactivity'

export default {
  components: {
    Header,
    AsideBar
  },
  setup () {
    const show = ref(false)

    const asideHandler = state => {
      show.value = state
    }
    return {
      show,
      asideHandler
    }
  }
}
</script>

<style lang="scss" scoped>
@import '@/assets/scss/transition.scss';
</style>