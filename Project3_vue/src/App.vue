<template>
  <header_comp :show_all="show_all" :show_films="show_films" :show_serials="show_serials" :show_cartoons="show_cartoons"></header_comp>
  <main>
    <card v-if="item_info == null" v-for="(el, i) in cards" :key="el.id" :index="i" :el_c="el" :show_item="show_item"/>
    <Item v-if="item_info != null" :item_info="item_info"></Item>
  </main>
  
  <footer_comp></footer_comp>
</template>

<script>
import Card from './components/card.vue';
import Footer_comp from './components/footer_comp.vue';
import Header_comp from './components/header_comp.vue';
import Item from './components/Item.vue';

  export default{
    components: {Card, Footer_comp, Header_comp, Item},
    data(){
      return{
        data_list: [
        {
        id:0,
        name:"Сверхестественное",
        logo:"/src/card_img/supernatural.jpg",
			  type:"serial",
        link:"https://supernatural-spn.online"
      },
		  {
        id:1,
		    name:"Во все тяжкие",
        logo:"/src/card_img/season-2.jpg",
			  type:"serial",
        link:"https://во-все-тяжкие.рф"
		  },
		  {
        id:2,
		    name:"Уэйн",
        logo:"/src/card_img/yein.jpg",
			  type:"serial",
        link:"https://hd.lordserial6.life/254-ujejn-2019.html"
		  },
		  {
        id:3,
		    name:"Пацаны",
        logo:"/src/card_img/the_boys.jpg",
			  type:"serial",
        link:"https://lordserial-o.net/3135-pacany.html"
		  },
		  {
        id:4,
		    name:"Кунгфу панда 4",
        logo:"/src/card_img/panda.jpg",
			  type:"cartoon",
        link:"https://po.kung-fu-panda-lordfilm.net/4-chast/"
		  },
		  {
        id:5,
		    name:"Неуйзвимий",
        logo:"/src/card_img/Invincible.jpg",
			  type:"cartoon",
        link:"https://hd1.26lordserial.xyz/1282-neuiazvimyi-sv-38.html"
		  },
		  {
        id:6,
		    name:"Не шутите с Зоханом",
        logo:"/src/card_img/zohan.jpg",
			  type:"film",
        link:"https://tv.lordfilmi.org/921-film-ne-shutite-s-zohanom.html"
		  },
		  {
        id:7,
		    name:"Стекло",
        logo:"/src/card_img/steklo.jpg",
			  type:"film",
        link:"https://star-wars-lordfilm.com/film/steklo"
		  },
		  {
        id:8,
		    name:"ВСЕГДА ГОВОРИ ДА",
        logo:"/src/card_img/yes.jpg",
			  type:"film",
        link:"https://tv.lordfilmi.org/1019-film-vsegda-govori-da.html"
		  }
    ],
        cards: [],
        item_info: null
      }
    },
    methods: {
      show_films(){
        this.item_info = null;
        console.log('Show Films');
        this.cards = [];
        for(var i=0; i<this.data_list.length; i++){
          if(this.data_list[i].type=="film"){
            this.cards.push(this.data_list[i]);
          }
        }
      },
      show_serials(){
        this.item_info = null;
        console.log('Show Serials');
        this.cards = [];
        for(var i=0; i<this.data_list.length; i++){
          if(this.data_list[i].type=="serial"){
            this.cards.push(this.data_list[i]);
          }
        }
      },
      show_cartoons(){
        this.item_info = null;
        console.log('Show Cartoons');
        this.cards = [];
        for(var i=0; i<this.data_list.length; i++){
          if(this.data_list[i].type=="cartoon"){
            this.cards.push(this.data_list[i]);
          }
        }
      },
      show_all(){
        this.cards = this.data_list;
        this.item_info = null;
      },
      show_item(i){
        this.item_info = this.data_list[i];
      }
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
