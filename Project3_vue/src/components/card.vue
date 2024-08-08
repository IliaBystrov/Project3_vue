<template>
  <div class="card_info" :key="index" @click="show_item(el_c.id)">
    <img v-bind:src="imageUrl" class="card_img"/>
    <p>{{ el_c.name }}</p>
  </div>
</template>

<script>
  export default{
    props:{
      el_c:{
        type: Object,
        requared: true
      },
      index:{
        type: Number,
        requared: true
      },
      show_item:{
        type:Function,
        requared:true
      }
    },
    data(){
      return{
        imageUrl: this.el_c.logo
      }
    }
  } 
</script>

<style scoped>
.card_info{
  display: flex;
  flex-direction: column;
  width: 200px;
  height: 300px;
  background: rgba(255, 255, 255, 0.7);
  border-radius: 5px;
  margin-left: 30px;
  margin-top: 30px;

  transition: transform 500ms ease;
}
.card_info:hover{
  transform: translateY(-15px);
  cursor: pointer;
  background: linear-gradient(169deg, rgba(179,75,255,0.8) 0%, rgba(252,252,252,0.5) 100%);
}
.card_info:active{
  transform: scale(0.9);
}
img{
  height: 250px;
  width: 190px;

  margin-top: 5px;
  margin-left: auto;
  margin-right: auto;
}
p{
  margin-top: auto;
  margin-bottom: auto;

  font-family: "Istok Web", sans-serif;
  font-size: 16px;
  font-weight: bold;

  background-image: linear-gradient(120deg, rgba(204,0,255,1) 0%, rgba(101,77,255,1) 100%);
  color: transparent;
  background-clip: text;
  -webkit-background-clip: text;
  
  display: flex;
  flex-direction: column;
  text-align: center;
}
</style>
