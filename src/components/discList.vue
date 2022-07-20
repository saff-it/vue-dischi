<template>

    <div>

        <div class="form-floating">
            <select class="form-select" id="floatingSelect" aria-label="Floating label select example">
                <option selected>Scegli l'album</option>
                <option value="1">One</option>
                <option value="2">Two</option>
                <option value="3">Three</option>
            </select>
            <label for="floatingSelect">Filtra per album</label>
        </div>

        <section>
            <discCard v-for="(card, index) in comicCards"
                :key="index"
                    :singleCard="card"
            />
        </section>

    </div>

    


</template>

<script>
import axios from 'axios';
import discCard from './discCard.vue'


export default {
    name: 'discList',
    components: {
        discCard,
    },

    data: function () {
        return {
            comicCards: [],
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
        }
    },

    created() {
        this.getAllCards();
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