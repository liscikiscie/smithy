<template>
    <div class="home-container">
        <div class="cover-mask"></div>
    </div>
</template>

<script>

    export default {
        name: 'home'
    }
</script>

<style lang="scss" scoped>
    @import "../scss/main";

    .home-container {
        background-image: url("../assets/images/header/city-bcg-photo.png");
        background-position: center;
        background-repeat: no-repeat;
        background-attachment: fixed;
        background-size: cover;
        height: 100vh;
        width: 100vw;

        .cover-mask {
            background-color: $mainDarkColor;
            opacity: .9;
            position: absolute;
            top: 0;
            left: 0;
            width: 100vw;
            height: 100vh;
        }
    }

</style>
