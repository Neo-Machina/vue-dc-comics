<template>
  <div id="app">
    <PageHeader />

    <main>
      <ComicsSection />
    </main>

    <Footer />
  </div>
</template>

<script>
import PageHeader from "./components/PageHeader.vue";
import ComicsSection from "./components/ComicsSection.vue"

export default {
  name: 'App',
  components: {
    PageHeader,
    ComicsSection
  }
}
</script>

<style lang="scss">
@import './style/common'
</style>
