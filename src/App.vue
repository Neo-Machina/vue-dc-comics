<template>
  <div id="app">
    <PageHeader />

    <main>
      <ComicsSection />
      <IconSection />
    </main>

    <Footer />
  </div>
</template>

<script>
import PageHeader from "./components/PageHeader.vue";
import ComicsSection from "./components/ComicsSection.vue";
import IconSection from "./components/IconSection.vue";


export default {
  name: 'App',
  components: {
    PageHeader,
    ComicsSection,
    IconSection
  }
}
</script>

<style lang="scss">
@import './style/common'
</style>
