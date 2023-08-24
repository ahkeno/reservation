<script setup>
import { ref,reactive } from 'vue'
import RestuarantListView from './RestuarantListView.vue';
const names = ref([
               { id: 1, name: 'La Pie Sa', openingHour: "9am", closingHour: "8pm", rating: "5 stars" },
               { id: 2, name: 'Lotteria' ,openingHour: "9am", closingHour: "8pm", rating: "2 stars"},
               { id: 3, name: 'Ya Kun',openingHour: "9am", closingHour: "8pm", rating: "3 stars" },
               { id: 4, name: 'Cha time' ,openingHour: "9am", closingHour: "8pm", rating: "4 stars"},
               { id: 5, name: 'Paradise Hotpot',openingHour: "9am", closingHour: "8pm", rating: "4 stars" },
               { id: 6, name: 'Daejeon BBQ' ,openingHour: "9am", closingHour: "8pm", rating: "3 stars"}
            ])
</script>
<template class="type-container">
   <div class="type-view" >
      <h2>Restuarant Types</h2>
      <span>Browse All</span>
      
      
     
   </div>
   <session class="item-session">
         <RestuarantListView 
         v-for="item in names"
         :key="item.id"
         :list="item"></RestuarantListView>
      </session>
</template>
<script>
import { RouterLink, RouterView } from 'vue-router'
export default {
  components: {  },
  data() {
    return {
      data: null,
    };
  },
  methods: {
    async routData() {
      router.push({ path: '/detail' })
    }
  }
};
</script> 
<style scoped>
.type-container{
   border: 1px solid red;
}
.type-view{
   display: flex;
   justify-content: space-between;
   border: 1px solid #000;
}
.item-session{
   display: flex;
}
</style>


