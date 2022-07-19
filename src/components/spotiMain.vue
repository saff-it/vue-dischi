<template>
    <main>
        <div class="container">
            <section>
                <discList />

            </section>
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

section{
    display: flex;
    flex-wrap: wrap;
}

div.ms_disc-container {
    height: 350px;
    width: calc(100% / 5 - 40px);
    color: white;
    text-align: center;
    background-color: $cardColorBg;
    padding: 18px;
    margin: 20px;

    img {
        width: 90%;
        height: 50%;
        object-fit: cover;
        object-position: top;
    }

    h3 {
        text-transform: uppercase;
        font-size: 1.2rem;
        margin: 12px 0;
    }

    span {
        color: rgb(104, 102, 102);
    }

}

</style>