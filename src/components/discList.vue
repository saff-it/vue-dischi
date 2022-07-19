<template>

    <section>
        <discCard />

    </section>
    

</template>

<script>
import discCard from './discCard.vue'


export default {
  name: 'discList',
  components: {
    discCard,
    
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