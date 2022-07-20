<template>

    <div>

        <section>
            <div class="form-floating">
                <select class="form-select" v-model="genre" @change="getConsoleLogSelect()" id="floatingSelect">
                    <option selected>Seleziona il genere</option>
                    <option value="Rock"> Rock </option>
                    <option value="Pop"> Pop </option>
                    <option value="Jazz"> Jazz </option>
                    <option value="Metal"> Metal </option>
                </select>
                <label for="floatingSelect">Filtra per genere</label>
            </div>

        </section>


        <section>
            <discCard v-for="(card, index) in comicCards" :key="index"
             :singleCard="card"
        />
        </section>

    </div>

</template>

<script>
import axios from 'axios';
import discCard from './discCard.vue';


export default {
    name: 'discList',
    components: {
        discCard,

    },

    data: function () {
        return {
            comicCards: [],
            discGenres: [],
            genre: '',
        }

    },

    methods: {
        getAllCards() {
            axios.get('https://flynn.boolean.careers/exercises/api/array/music')
                .then((result) => {
                    this.comicCards = result.data.response;
                    console.log(result.data.response);
                })
                .catch((error) => {
                    console.log(error);
                })
        },

        getMusicGenres() {
            this.comicCards.forEach((card) => {
                if(!this.discGenres.includes(card.genre)){
                    this.discGenres.push(card.genre);
                }

            })
            
        },

        getConsoleLogSelect(){
            console.log(this.genre);
        }


    },

    created() {
        this.getAllCards();
        this.getMusicGenres();
    }


}

</script>

<style lang="scss">
@import "../styles/general.scss";
@import "../styles/variables.scss";

section {
    display: flex;
    flex-wrap: wrap;
}
</style>