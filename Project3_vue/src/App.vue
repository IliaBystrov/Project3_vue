<template>
  <header_comp></header_comp>
</template>

<script>
import Card from './components/card.vue';
import Footer_comp from './components/footer_comp.vue';
import Header_comp from './components/header_comp.vue';

  export default{
    components: {Card, Footer_comp, Header_comp},
    data(){
      return{
        data_list: [],
        cards: [],

      }
    },
    computed: {

    },
    methods: {

    }
  } 
</script>

<style scoped>
</style>
