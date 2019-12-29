<template>
    <div class="logos-wrapper">
        <h2>Find Best Logos</h2>
        <div class="item-logos">
            <img class="film-logos" alt="Film logo" src="../assets/film.png">
        </div>
    </div>
</template>

<script>
export default {
    name: 'Logos',    
}
</script>

<style scoped>
.logos-wrapper{
    width: 70%;
    overflow: hidden;
    margin: auto;
}

.item-logos{
    float: left;
    width: 150px;
    height: 150px;
    margin-right: 20px;
    margin-bottom: 20px;
}

.item-logos .film-logos{
    width: 150px;
    height: 150px;
}
</style>

