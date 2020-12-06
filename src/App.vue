<template>
  <div id="app">

    <div id="news" class="container-fluid alert alert-dark">
      <section-api></section-api>
    </div>

    <div id="team" class="alert alert-light">
      <!-- TEAM -->
    </div>
    
  </div>

</template>

<script>
import SectionApi from './components/SectionApi.vue'

export default {
  components: { SectionApi },
  name: 'App',
}
</script>

