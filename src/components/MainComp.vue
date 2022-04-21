<template>
    <main class="main">
        <DischiComp
        v-for="(element, index) in AlbumArray"
        :key="index"
        :author="element.author"
        :image="element.poster"
        :title="element.title"
        :year="element.year"
        />
    </main>
</template>

<script>
    import axios from 'axios';
    import DischiComp from './partials/DischiComp.vue'

    export default {

        name: 'MainComp',
        comments: {
            DischiComp
        },

        data() {
            return {
                AlbumArray: []
            }
        },
        created() {
            axios.get('https://flynn.boolean.careers/exercises/api/array/music')
                .then((res) => {
                    console.log(res.data);
                    this.AlbumArray = res.data
                })
                .catch((error) => {
                    console.log(error)
                })
        }
    }
</script>

<style scoped lang="scss">
    .main {
        background-color: #202B39;
        height: 95vh;
    }
</style>