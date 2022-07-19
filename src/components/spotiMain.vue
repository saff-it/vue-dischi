<template>
    <main>
        <div class="container">

            <section>
                <div class="ms_disc-container">
                    <img src="https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2018/09/AC1000_DLX_162-001_HD_5ba13723281ab0.37845353.jpg?itok=ZsI-C5eX"
                        alt="Disc Cover">
                    <h3>New Jersey</h3>
                    <span>Bob Joviu <br> 1190</span>
                </div>
            </section>

        </div>
    </main>
</template>

<script>
import discList from './components/discList.vue'



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