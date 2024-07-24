<template>
    <div class="header_comp">
        <img src="" class="logo">
        <h1>Кино-Сериалы-Мультики</h1>
    </div>
</template>

<script>
  export default{
    data(){

    },
    computed: {

    },
    methods: {
      
    }
  } 
</script>

<style scoped>
.header_comp{
    width: 100%;
    height: 120px;
    background: rgb(255,220,130);
    background: linear-gradient(120deg, rgba(255,220,130,1) 0%, rgba(255,100,100,1) 100%);
    display: flex;
    flex-wrap: wrap;
    box-shadow: 0px 2px 5px rgba(255, 212, 128, 1);
}
img{
    width: 90px;
    height: 90px;
}
h1{
    background-image: linear-gradient(120deg, rgba(204,0,255,1) 0%, rgba(101,77,255,1) 100%);
    color: transparent;
    background-clip: text;
    -webkit-background-clip: text;
    font-size: 32px;
}
</style>
