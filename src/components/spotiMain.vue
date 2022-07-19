<template>
    <main>
        <div class="container">
            <discList />
            
        </div>
    </main>
</template>

<script>
import discList from './discList.vue'



export default {
  name: 'spotiMain',
  components: {
    discList,
    
  }
}

</script>


<style lang="scss" scoped>
@import "../styles/general.scss";
@import "../styles/variables.scss";

div.container {
    margin-top: 70px; 
}


</style>