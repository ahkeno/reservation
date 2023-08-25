<script  setup lang="ts" >
import RestuarantTypeVue from '../components/RestuarantType.vue';
import SearchView from '../components/SearchView.vue';
</script>
<template>
  <main>
  <session>
    <SearchView></SearchView>
  </session>
  <section>
    this is Promotion Component
  </section>
  <section>
    this is Top Reated Component
  </section>
  <section>
    <RestuarantTypeVue/>
  </section>
</main>
</template>
<style scope>
.home-view
{
  border: 1px solid red;
}
</style>
