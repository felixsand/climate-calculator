<template>
  <section>
    <b-tabs v-model="activeTab">
      <b-tab-item label="Dwelling">
        <Dwelling></Dwelling>
      </b-tab-item>

      <b-tab-item label="Travel">
        <Travel></Travel>
      </b-tab-item>

      <b-tab-item label="Food">
        <Food></Food>
      </b-tab-item>

      <b-tab-item label="Consumption">
        <Consumption></Consumption>
      </b-tab-item>

      <b-tab-item label="Results" disabled>
        <Results></Results>
      </b-tab-item>
    </b-tabs>
  </section>
</template>

<script>
  import Vue from 'vue'
  import Buefy from 'buefy'
  import 'buefy/dist/buefy.css'
  import Dwelling from "./components/forms/Dwelling";
  import Consumption from "./components/forms/Consumption";
  import Food from "./components/forms/Food";
  import Travel from "./components/forms/Travel";
  import Results from "./components/Results";

  Vue.use(Buefy)

  export default {
    name: 'app',
    components: {
      Consumption,
      Food,
      Travel,
      Dwelling,
      Results
    },
    data() {
      return {
        activeTab: 0
      }
    }
  }
</script>

<style>

</style>
