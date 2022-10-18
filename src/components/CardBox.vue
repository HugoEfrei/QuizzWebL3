<template>
  <div class="col" :style="cardStyle">
    <img class="cafe" :src="require(`@/assets/${source}`)" alt="Something">
    <p class="coffee_name">{{coffee_name}}&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;{{price}}</p>
    
    <button @click="toHot">Hot</button>
    <button @click="toCold">Cold</button>
  </div>
</template>
  
<script>
  export default {
    name : "CardBox",
    data() {
      return {
        cardStyle: {}
      }
    },
    props : {
      coffee_name : String,
      source : String,
      price: String
    },
    methods :{
      toHot () {
        this.cardStyle.backgroundColor = 'rgb(230, 112, 69, .8)'
      },
      toCold () {
        this.cardStyle.backgroundColor = 'rgb(146, 222, 222,.8)'
      }
    },
    created() {
      console.log(this.cardStyle)
    }
  }
</script>
  
<style>
  .coffee_name{
    font-size: 23px ;
  }  

  .col{
    background-color: rgb(194, 142, 46, .8);
    border-radius: 5%;
    height: 300px;
    width: auto;
    padding: 2%;
    margin: 3%;
  }
</style>