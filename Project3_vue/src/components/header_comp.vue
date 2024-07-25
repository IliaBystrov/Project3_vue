<template>
    <div class="header_comp">
        <img src="/src/img/logo.png" class="logo" @click="show_all()">
        <h1 @click="show_all()">Кино-Сериалы-Мультики</h1>

        <div class="btn_block">
            <button @click="show_films()"><h2>Кино</h2></button>
            <button @click="show_serials()"><h2>Сериалы</h2></button>
            <button @click="show_cartoons()"><h2>Мультики</h2></button>
        </div>
    </div>
</template>

<script>
  export default{
    props:{
        show_films:{
            type: Function,
            requare: true
        },
        show_serials:{
            type: Function,
            requare: true
        },
        show_cartoons:{
            type: Function,
            requare: true
        },
        show_all:{
            type: Function,
            requare: true  
        }
    },
    /*data(){

    },*/
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
    align-items: center;
}
img{
    width: 90px;
    height: 90px;
    margin-left: 16px;
    transition: transform 200ms ease;
    cursor: pointer;
}
img:hover{
    transform: scale(1.1);
}
img:active{
    transform: scale(0.9);
}
h1{
    background-image: linear-gradient(120deg, rgba(204,0,255,1) 0%, rgba(101,77,255,1) 100%);
    color: transparent;
    background-clip: text;
    -webkit-background-clip: text;

    font-size: 32px;
    margin-left: 28px;

    transition: transform 200ms ease;
    cursor: pointer;
    font-family: "Istok Web", sans-serif;
}
h1:hover{
    background-image: linear-gradient(120deg,rgba(101,77,255,1) 100%, rgba(204,0,255,1) 0%);
    color: transparent;
    background-clip: text;
    -webkit-background-clip: text;
    transform: scale(1.05);
}
h1:active{
    transform: scale(0.9);
}
.btn_block{
    margin-left: auto;
}
.btn_block button{
    margin-right: 10px;
    width: 300px;
    height: 100px;
    border: 0px;
    border-bottom: 3px solid ;

    border-image: linear-gradient(120deg, rgba(204,0,255,1) 0%, rgba(101,77,255,1) 100%);
    -moz-border-image: -moz-linear-gradient(120deg, rgba(204,0,255,1) 0%, rgba(101,77,255,1) 100%);
    -webkit-border-image: -webkit-linear-gradient(120deg, rgba(204,0,255,1) 0%, rgba(101,77,255,1) 100%);
    border-image-slice: 1;

    background-color: rgba(217, 217, 217, 0.2);
    color: rgba(0, 0, 0, 1);

    transition: transform 200ms ease;
    cursor: pointer;

}
.btn_block button:hover{
    transform: scale(0.9);
    background: rgba(101,77,255,0.2);
}
.btn_block button:active{
    transform: scale(0.6);
    background: rgba(101,77,255,0.5);
}
button h2{
    background-image: linear-gradient(120deg, rgba(204,0,255,1) 0%, rgba(101,77,255,1) 100%);
    color: transparent;
    background-clip: text;
    -webkit-background-clip: text;
    font-size: 32px;
    font-family: "Istok Web", sans-serif;
}
</style>
