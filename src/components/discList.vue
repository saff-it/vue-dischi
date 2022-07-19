<template>

    <section>
        <discCard v-for="(card, index) in cards"
        :key="index" 
            :singleCard="card"
        />

    </section>
    

</template>

<script>
import axios from 'axios';
import discCard from './discCard.vue'


export default { 
  name: 'discList',
  components: {
    discCard,
  },

  data: function() {
    return{
        cards: [],
    }
  }, 

  methods:{
    getSingleCard(){
        axios.get('https://flynn.boolean.careers/exercises/api/array/music')
        .then((result) => {
            this.cards.push(result.data.response);
        })
        .catch((error) => {
            console.log(error);
        })
    }
  },

  created(){
    this.getSingleCard();
  }
    
    
}

</script>

<style lang="scss">
@import "../styles/general.scss";
@import "../styles/variables.scss";

section{
    display: flex;
    flex-wrap: wrap;
}


</style>