<template>
    <div class="item_block">
        <div class="t_i">
            <h1>{{ item_info.name }}</h1>
            <img v-bind:src="imageUrl" class="card_img"/>
        </div>
        <div class="about">
            <p>
                Описание. 
                10100101001010101001010111101010101001010010101010101010101010101010
            </p>
        </div>
    </div>
    <div class="item_content">
        <a v-bind:href="item_info.link" target="_blank">Перейти на страницу</a>
        <iframe width="1000" height="600" v-bind:src="item_info.link"></iframe>
    </div>
</template>
  
<script>
export default{
    props:{
        item_info:{
            tepe: Object,
            requared: true
        }
    },
    data(){
    return{
        imageUrl: this.item_info.logo
        }
    }

} 
</script>
  
<style scoped>
.item_block{
    display: flex;
    flex-direction: row;
    margin-top: 30px;
    margin-left: 30px;
    margin-right: 30px;
    width: 100%;
}
.t_i{
    text-align: center;
}
.about{
    width: 100%;
    margin-left: 30px;
    margin-right: 30px;

    align-content: center;
}
img{
    height: 350px;
    width: 250px;
    margin-top: 5px;
    border: 3px solid rgba(101,77,255,1);
    border-radius: 10px;
}
h1{
    background-image: linear-gradient(120deg, rgba(204,0,255,1) 0%, rgba(101,77,255,1) 100%);
    color: transparent;
    background-clip: text;
    -webkit-background-clip: text;
    font-family: "Istok Web", sans-serif;
}
p{
    font-size: 25px;
    font-weight: 600;
    font-family: "Istok Web", sans-serif;
}
.item_content{
    display: flex;
    flex-direction: column;

    text-align: center;

    margin-left: auto;
    margin-right: auto;
    margin-top: 30px;
}
a{
    font-family: "Istok Web", sans-serif;
    font-size: 25px;
    font-weight: 600;
    color: green;
    text-decoration: none;
    margin-bottom: 20px;
    transition: transform 1000ms ease;
    
}
a:hover{
    transform: scale(1.1);
    animation: color-change 5s infinite;
}
@keyframes color-change {
  0% { color: rgba(101,77,255,1); }
  50% { color: rgb(255, 59, 82); }
  100% { color: rgba(101,77,255,1); }
}
iframe{
    border-radius: 10px;
    border: 3px solid rgba(101,77,255,1);
}
</style>
  