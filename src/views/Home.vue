<template>
    <div class="home-container">
        <div class="project-description">
            <div class="description-wrapper">
                <h1 class="project-name">{{ projectName }}</h1>
                <h2 class="project-motto">{{ projectMotto }}</h2>
                <p class="moveOn-link">
                    {{ goAhead }}
                    <font-awesome
                            class="arrow-icon"
                            icon="angle-double-right"
                    />
                </p>
            </div>
        </div>
        <div class="social-media-panel">
            <a class="outer-links"
               href="https://allegro.pl/oferta/hoker-barowy-obrotowy-stolek-profilowany-kuchenny-6645426037?fromVariant=6913254833"
               target="_blank">
                <font-awesome
                        class="arrow-icon icons"
                        icon="angle-double-right"
                />
            </a>
        </div>
        <div class="cover-lightMask">
            <span class="letter-orange">S</span>
        </div>
    </div>
</template>

<script>

    export default {
        name: 'home',
        data() {
            return {
                projectName: 'SMITHY',
                projectMotto: 'WEB APPS NOT ONLY FOR YOU',
                goAhead: 'READ MORE'

            }
        }
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

    @font-face {
        font-family: 'Nunitoregular';
        src: url('../assets/fonts/Nunito/nunito-regular.eot');
        src: url('../assets/fonts/Nunito/nunito-regular.eot?#iefix') format('embedded-opentype'),
        url('../assets/fonts/Nunito/nunito-regular.woff2') format('woff2'),
        url('../assets/fonts/Nunito/nunito-regular.woff') format('woff'),
        url('../assets/fonts/Nunito/nunito-regular.ttf') format('truetype'),
        url('../assets/fonts/Nunito/nunito-regular.svg#nunitoregular') format('svg');
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
        position: relative;

        .social-media-panel {
            width: 100vw;
            height: 100vh;
            display: flex;
            justify-content: flex-end;
            align-items: center;
            cursor: default;
            user-select: none;

            .outer-links {
                margin-right: 35px;
                color: white;

                .icons {
                    font-size: 30px;

                }
            }
        }

        .project-description {
            height: 100vh;
            display: flex;
            justify-content: center;
            align-items: center;
            margin-right: 685px;
            cursor: default;
            user-select: none;
            z-index: 2;

            .description-wrapper {
                display: flex;
                justify-content: flex-start;
                align-items: flex-start;
                flex-flow: column wrap;

                .project-name {
                    font-size: 72px;
                    color: white;
                    z-index: 1;
                    font-family: DeathStar, sans-serif;
                    letter-spacing: 45px;
                    margin-left: 250px;
                }

                .project-motto {
                    font-size: 21px;
                    color: $secondaryFontColor;
                    z-index: 1;
                    font-family: DeathStar, sans-serif;
                    letter-spacing: 12px;
                    margin: 20px 0 0 250px;

                }

                .moveOn-link {
                    font-size: 18px;
                    font-family: Nunitoregular, sans-serif;
                    color: white;
                    z-index: 1;
                    margin: 30px 0 0 250px;
                    padding-top: 30px;
                    transition: text-shadow .3s;
                    border-top: 2px solid $mainLightColor;

                    .arrow-icon {
                        margin-left: 15px;
                        color: $mainLightColor;
                    }

                    &:hover {
                        text-shadow: 0 0 .65px #fff, 0 0 .65px #fff;
                        cursor: pointer;
                    }
                }
            }
        }

        .social-media-panel {
            display: flex;
            justify-content: flex-end;
            align-items: center;
        }
    }

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
        cursor: default;
        user-select: none;

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

</style>
