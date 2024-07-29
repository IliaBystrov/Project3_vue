<template>
  <header_comp :show_all="show_all" :show_films="show_films" :show_serials="show_serials" :show_cartoons="show_cartoons"></header_comp>
  <main>
    <card v-for="(el, i) in cards" :key="el.id" :index="i" :el_c="el"/>
  </main>
  
  <footer_comp></footer_comp>
</template>

<script>
import Card from './components/card.vue';
import Footer_comp from './components/footer_comp.vue';
import Header_comp from './components/header_comp.vue';

  export default{
    components: {Card, Footer_comp, Header_comp},
    data(){
      return{
        data_list: [
        {
        id:0,
        name:"Сверхестественное",
        logo:"/src/card_img/supernatural.jpg",
			  type:"serial"
      },
		  {
        id:2,
		    name:"Во все тяжкие",
        logo:"/src/card_img/season-2.jpg",
			  type:"serial"
		  },
		  {
        id:3,
		    name:"Уэйн",
        logo:"/src/card_img/yein.jpg",
			  type:"serial"
		  },
		  {
        id:4,
		    name:"Пацаны",
        logo:"/src/card_img/the_boys.jpg",
			  type:"serial"
		  },
		  {
        id:5,
		    name:"Кунгфу панда 4",
        logo:"/src/card_img/panda.jpg",
			  type:"cartoon"
		  },
		  {
        id:6,
		    name:"Неуйзвимий",
        logo:"/src/card_img/Invincible.jpg",
			  type:"cartoon"
		  },
		  {
        id:7,
		    name:"Не шутите с Зоханом",
        logo:"/src/card_img/zohan.jpg",
			  type:"film"
		  },
		  {
        id:8,
		    name:"Стекло",
        logo:"/src/card_img/steklo.jpg",
			  type:"film"
		  },
		  {
        id:9,
		    name:"ВСЕГДА ГОВОРИ ДА",
        logo:"/src/card_img/yes.jpg",
			  type:"film"
		  }
    ],
        cards: []
      }
    },
    computed: {

    },
    methods: {
      show_films(){
        console.log('Show Films');
        this.cards = [];
        for(var i=0; i<this.data_list.length; i++){
          if(this.data_list[i].type=="film"){
            this.cards.push(this.data_list[i]);
          }
        }
      },
      show_serials(){
        console.log('Show Serials');
        this.cards = [];
        for(var i=0; i<this.data_list.length; i++){
          if(this.data_list[i].type=="serial"){
            this.cards.push(this.data_list[i]);
          }
        }
      },
      show_cartoons(){
        console.log('Show Cartoons');
        this.cards = [];
        for(var i=0; i<this.data_list.length; i++){
          if(this.data_list[i].type=="cartoon"){
            this.cards.push(this.data_list[i]);
          }
        }
        this.$forceUpdate();
      },
      show_all(){
        this.cards = this.data_list;
      },
    },
  } 
</script>

<style scoped>
main{
  display: flex;
  flex-wrap: wrap;
  margin-bottom: 30px;
}

</style>
