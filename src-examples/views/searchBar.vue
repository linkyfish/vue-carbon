<template>
  <div class="vc-page">
    <header-bar>
      <icon-button slot="left" @click="back()" icon="arrow_back"></icon-button>
      <span>Search Bar</span>
    </header-bar>
    <search-bar :focus.sync="focus"></search-bar>
    <scroll-view>
      <overlay v-if="focus"></overlay>
    </scroll-view>
  </div>
</template>

<script>
export default {
  methods: {
    back () {
      window.history.back()
    }
  },
  data () {
    return {
      focus: false
    }
  }
}
</script>

<style lang="css">

</style>
