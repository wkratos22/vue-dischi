<template>
    <div class="header">
        <img class="logo inline" src="../assets/spotify-2.svg" alt="logo spotify">

        <select class="form-select inline" aria-label="Default select example">
            <option selected>Rock</option>
            <option value="1">Pop</option>
            <option value="2">Jazz</option>
            <option value="3">Metal</option>
            <option value="3">Rock</option>
        </select>
    </div>
</template>

<script>
export default {
  name: 'HeaderComp',
}
</script>

<style scoped lang="scss">
    .header{
        background-color: rgb(50, 52, 71);
        padding: 10px;
    }
    .logo{
        width: 40px;
    }

    .form-select{
        width: 100px;
        vertical-align: middle;
        margin-left: 90%;
    }

    .inline{
        display: inline-block;
    }
</style>