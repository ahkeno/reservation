

<template>
  <div class="detail-view">
    <h3>
      This is detail {{ title }}
      <pre>id: {{ id }}</pre>
    </h3>
  </div>
</template>

<script lang="ts">
import { computed } from "vue";
import { useRoute } from "vue-router";
export default {
  name: "App",
  props: ['title'],
  setup() {
   
    const route = useRoute();
    const id = computed(() => route.params.id);
    return {
      id,
    };
  },
};
</script>
<style scoped>
h1 {
  font-weight: 500;
  font-size: 2.6rem;
  position: relative;
  top: -10px;
}

h3 {
  font-size: 1.2rem;
}
.detail-view
{
  border: 1px solid #000;
}
@media (min-width: 1024px) {
  .greetings h1,
  .greetings h3 {
    text-align: left;
  }
}
</style>
