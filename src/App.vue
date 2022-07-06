<template>
  <div id="app">
    <PageHeader />

    <main>

    </main>

    <Footer />
  </div>
</template>

<script>
import PageHeader from "./components/PageHeader.vue";

export default {
  name: 'App',
  components: {
    PageHeader
  }
}
</script>

<style lang="scss">
@import './style/common'
</style>
