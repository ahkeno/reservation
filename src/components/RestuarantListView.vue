<script setup>
import Router from '../router';
defineProps(['list'])

function onClickList(id){
  console.log("on click list iteme",id)
  Router.push('/detail/'+id)
}
</script>
<template>
    <div class="item-container" @click="onClickList(list.id)">
      <h2> {{list.name}}</h2>
      <h3>
         Opening Hour: {{ list.openingHour }}
      </h3>
      <h3>
         Closing Hour: {{ list.closingHour }}
      </h3>
   </div>
  
   
</template>
<script>
import { RouterLink, RouterView } from 'vue-router'
export default {
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

.item-container{
   border: 1px solid #000;
   padding: 2px;
   margin: 5px;
}
</style>


