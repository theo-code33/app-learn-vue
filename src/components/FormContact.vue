<template>
    <form @submit.prevent="handleSubmit">
        <input type="text" placeholder="Le titre du site" v-model="credentials.title">
        <input type="text" placeholder="Durée du film" v-model="credentials.duration">
        <input type="text" placeholder="Notation du film" v-model="credentials.notation">
        <input type="submit" value="Envoyer">
    </form>

    <FilmsList :filmsList="filmsList" />
</template>

<script>
import FilmsList from "@/components/FilmsList.vue";

export default {
    name: 'FormContact',
    components: {
        FilmsList
    },
    data(){
        return {
            credentials: {
                title: '',
                duration: '',
                notation: '',
            },
            filmsList: []
        }
    },
    methods:{
        handleSubmit(){
            console.log("Credential ",this.credentials);
            console.log("FilmsList",this.filmsList);
            this.filmsList.push(this.credentials);

            this.credentials = {
                title: '',
                duration: '',
                notation: '',
            }
        }
    }
}
</script>