<template>
    <main class="main">
        
    </main>
</template>

<script>
    import axios from 'axios';

    export default {

        name: 'MainComp',
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
    }
</style>