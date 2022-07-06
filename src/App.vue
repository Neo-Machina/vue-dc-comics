<template>
  <div id="app">
    <PageHeader />

    <main>
      <ComicsSection />
      <IconSection />
    </main>

    <PageFooter />
  </div>
</template>

<script>
import PageHeader from "./components/PageHeader.vue";
import ComicsSection from "./components/ComicsSection.vue";
import IconSection from "./components/IconSection.vue";
import PageFooter from "./components/PageFooter.vue";


export default {
  name: 'App',
  components: {
    PageHeader,
    ComicsSection,
    IconSection,
    PageFooter
  }
}
</script>

<style lang="scss">
@import './style/common'
</style>
