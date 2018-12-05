<template>
    <div class="home-container">
        <div class="cover-lightMask">
            <span class="letter-orange">S</span>
        </div>
    </div>
</template>

<script>

    export default {
        name: 'home'
    }
</script>

<style lang="scss" scoped>
    @import "../scss/main";

    @font-face {
        font-family: 'DeathStar';
        src: url('../assets/fonts/DeathStar/death_star.eot');
        src: url('../assets/fonts/DeathStar/death_star.eot?#iefix') format('embedded-opentype'),
        url('../assets/fonts/DeathStar/death_star.woff2') format('woff2'),
        url('../assets/fonts/DeathStar/death_star.woff') format('woff'),
        url('../assets/fonts/DeathStar/death_star.ttf') format('truetype'),
        url('../assets/fonts/DeathStar/death_star.svg#death_starregular') format('svg');
        font-weight: normal;
        font-style: normal;

    }

    .home-container {
        background-image: url("../assets/images/header/city-bcg-photo.png");
        background-position: center;
        background-repeat: no-repeat;
        background-attachment: fixed;
        background-size: cover;
        height: 100vh;
        width: 100vw;

        .cover-lightMask {
            opacity: .8;
            position: absolute;
            top: 0;
            right: 0;
            width: 100vw;
            height: 100vh;
            display: flex;
            justify-content: center;
            align-items: center;
            background-color: $mainDarkColor;

            .letter-orange {
                background: url("../assets/images/header/city-bcg-photo.png") -743px  -155px;
                -webkit-text-fill-color: rgba(255, 66, 0, .5);
                -webkit-background-clip: text;
                font-size: 850px;
                font-family: DeathStar, sans-serif;

            }
        }

        .center-big-letter {
            font-size: 720px;
            color: #ff4200;
            opacity: .5;
        }
    }

</style>
