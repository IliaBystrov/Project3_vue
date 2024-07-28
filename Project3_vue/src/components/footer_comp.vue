<template>
  <div class="footer_comp">
    <a href="https://vk.com/dartvikt0r" target="_blank"><img src="/src/img/vk.png" class="social" /></a>
    <a href="https://t.me/dartvikt0r" target="_blank"><img src="/src/img/tg.png" class="social" /></a>
  </div>
</template>

<script>
  export default{
    computed: {

    },
    methods: {
      
    }
  } 
</script>

<style scoped>
.footer_comp{
  width: 100%;
  min-height: 120px;

  background: rgb(255,100,100);
  background: linear-gradient(90deg, rgba(255,100,100,1) 0%, rgba(255,220,130,1) 100%);

  box-shadow: 0px -2px 5px rgba(255, 212, 128, 1);

  display: flex;
  flex-wrap: wrap;
  align-items: center;
  margin-top: auto;
}
img{
  height: 50px;
  width: 50px;
  transition: transform 500ms ease;
  margin-left: 35px;
}
img:hover{
  cursor: pointer;
  transform: scale(1.2);
}
</style>
