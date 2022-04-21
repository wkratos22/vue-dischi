<template>
    <div class="main row">
        <DischiComp
        v-for="(element, index) in AlbumArray"
        :key="index"
        :author="element.author"
        :poster="element.poster"
        :title="element.title"
        :year="element.year"
        :genre="element.genre"
        />
    </div>
</template>

<script>
    import axios from 'axios';
    import DischiComp from './partials/DischiComp.vue'

    export default {

        name: 'MainComp',
        components: {
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