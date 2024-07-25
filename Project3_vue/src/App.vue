<template>
  <header_comp :show_all="show_all" :show_films="show_films" :show_serials="show_serials" :show_cartoons="show_cartoons"></header_comp>
  <main>
    <p>123</p>
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
        name:"Сверхестественное",
        logo:"/card_img/supernatural.jpg",
			  type:"serial"
      },
		  {
		    name:"Во все тяжкие",
        logo:"/card_img/season-2.jpg",
			  type:"serial"
		  },
		  {
		    name:"Уэйн",
        logo:"/card_img/yein.jpg",
			  type:"serial"
		  },
		  {
		    name:"Пацаны",
        logo:"/card_img/the_boys.jpg",
			  type:"serial"
		  },
		  {
		    name:"Кунгфу панда 4",
        logo:"/card_img/panda.jpg",
			  type:"cartoon"
		  },
		  {
		    name:"Неуйзвимий",
        logo:"/card_img/Invincible.jpg",
			  type:"cartoon"
		  },
		  {
		    name:"Не шутите с Зоханом",
        logo:"/card_img/zohan.jpg",
			  type:"film"
		  },
		  {
		    name:"Стекло",
        logo:"/card_img/steklo.jpg",
			  type:"film"
		  },
		  {
		    name:"ВСЕГДА ГОВОРИ ДА",
        logo:"/card_img/yes.jpg",
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
      },
      show_serials(){
        console.log('Show Serials');
      },
      show_cartoons(){
        console.log('Show Cartoons');
      },
      show_all(){
        console.log('Show ALL');
      }
    }
  } 
</script>

<style scoped>
main{
  display: flex;
  flex-wrap: wrap;
}

</style>
