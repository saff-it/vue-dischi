<template>

    <section>
        <discCard v-for="(card, index) in comicCards"
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
        comicCards: [],
    }
  }, 

  methods:{
    getAllCards(){
        axios.get('https://flynn.boolean.careers/exercises/api/array/music')
        .then((result) => {
            this.comicCards = result.data.response;
            console.log(result.data.response);
        })
        .catch((error) => {
            console.log(error);
        })
    }
  },

  created(){
    this.getAllCards();
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