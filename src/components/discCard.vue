<template>

    <div class="ms_disc-container">
        <img :src="singleCard.poster"
            alt="Disc Cover">
        <h3>{{singleCard.title}}</h3>
        <span>{{singleCard.author}} <br> {{singleCard.year}}</span>
    </div>

</template>

<script>
export default {
    props: ['singleCard'],
}
</script>

<style lang="scss">
@import "../styles/general.scss";
@import "../styles/variables.scss";


.ms_disc-container {
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