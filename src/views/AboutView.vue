<template>
 
  <div class="about">
    <h1 class="textcafe">Enjoy your <span class="wordcoffee">coffee</span> before your activity</h1>  
  </div>
  
  <div class="container text-center">
    <div class="row"> 
        <CardBox coffee_name="Vanilla Latte" source ="Vanilla-Latte.png" price="5$"></CardBox> 
        <CardBox coffee_name="Expresso" source="expresso.png" price="2$"></CardBox> 
        <CardBox coffee_name="Hazelnut-Latte" source="Hazelnut-Latte.png" price="7$"></CardBox> 
    </div>
    <div class="row"><CardBox v-for="item in CoffeeMenu" :key=item.id :coffee_name=item.coffee_name :source=item.source :price=item.price></CardBox></div>  
    <div class="row">
      <SlottedCard>
        <template #top><img class="cafe" src="../assets/moccacinno.png"></template>
        <template #middle><p class="coffee_name">Moccacinno&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;6$</p></template>
        <template #bottom><button>Soon to come</button></template>
      </SlottedCard>
    </div>
  </div>

</template>


<script>
  import CardBox from '@/components/CardBox.vue';
  import SlottedCard from '@/components/SlottedCard.vue';



export default {
    name: "AboutView",
    components: { CardBox, SlottedCard },
    data(){
      return {
        CoffeeMenu: [
          {coffee_name:"Vanilla Latte", price:"5$",source:"Vanilla-Latte.png"},
          {coffee_name:"Expresso", price:"2$",source:"expresso.png"},
          {coffee_name:"Hazelnut Latte", price:"7$",source:"Hazelnut-Latte.png"}]
      };
    },
    
    beforeMount(){
      var db = localStorage.getItem('menu')
      if(db){
        this.CoffeeMenu = JSON.parse(db)}
        else{
          var data = [
            {coffee_name:"Cappucino", price:"7$",source:"cappucino.png"},
            {coffee_name:"Chocolat", price:"5$",source:"chocolat.png"},
            {coffee_name:"Coffee Cream", price:"8$",source:"coffee-cream.png"},
        ]
        this.CoffeeMenu = localStorage.setItem('menu',JSON.stringify(data))
        }
    },

    beforeUnmount(){
        alert('You will exit this page');
    },  
}

</script>

<style>
  
  .about{
    padding: 40px;
    font-size: larger;
  }



  .col:hover{
    transform: scale(1.15);
    transition : all .2s ease;
  }

  .cafe {
    float: center;
    border-radius: 5%;
    height: 186px;
    width: auto;
    background-size: cover;
  }

  .textcafe{
    color: #E0924B;
    font-style: italic;
    font-family: "STXingkai";
  }

  .wordcoffee{
    color: rgb(165, 95, 42);
  }

  .foot{
    padding : 10px;
    position: right;
  }
</style>