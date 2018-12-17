<template>
    <main>
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
            <div class="cover-lightMask">
                <span class="letter-orange">S</span>
            </div>
        </div>
        <aside>
            <ul class="social-media-container">
                <li>
                    <a href="https://www.facebook.com/Smithy-285340225458595/?modal=admin_todo_tour"
                       target="_blank">
                        <img src="../assets/fonts/facebook-box.svg"
                             class="social-medial-icon"
                             alt="facebook-link"/>
                    </a>
                </li>
                <li>
                    <a href="https://twitter.com/lisci_kiscie"
                       target="_blank">
                        <img src="../assets/fonts/twitter-box.svg"
                             class="social-medial-icon"
                             alt="twitter-link"/>
                    </a>
                </li>
                <li>
                    <a href="https://github.com/liscikiscie"
                       target="_blank">
                        <img src="../assets/fonts/github-box.svg"
                             class="social-medial-icon"
                             alt="github-link"
                        />
                    </a>
                </li>
            </ul>
        </aside>
    </main>
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

    main {
        position: relative;

        aside {
            position: absolute;
            bottom: 0px;
            background-color: transparent;
            width: 100%;

            /*
                        position: absolute;
            top: 40%;
            right: 32px;
            background-color: transparent;
            width: 30px;
            height: 250px;
            */

            .social-media-container {
                height: 100%;
                display: flex;
                flex-direction: row;
                justify-content: space-around;
                align-items:  center;

                /*
                           height: 100%;
                display: flex;
                flex-direction: column;
                justify-content: space-evenly;*/

                .social-medial-icon {
                    width: 20px;
                }
            }
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

            .project-description {
                height: 100%;
                display: flex;
                justify-content: center;
                align-items: center;
                margin-right: 300px;
                cursor: default;
                user-select: none;
                z-index: 2;

                /*@media screen and (max-width: 320px) {*/
                    /*margin-right: 685px;*/
                /*}*/

                .description-wrapper {
                    display: flex;
                    justify-content: space-between;
                    align-items: flex-start;
                    flex-flow: column wrap;

                    .project-name {
                        display: none;
                        font-size: 22px;
                        color: white;
                        z-index: 1;
                        font-family: DeathStar, sans-serif;
                        letter-spacing: 20px;
                        margin-left: 350px;

                        /*@media screen and (max-width: 320px) {
                        font-size: 22px;
                        color: white;
                        z-index: 1;
                        font-family: DeathStar, sans-serif;
                        letter-spacing: 45px;
                        margin-left: 250px;
                        /*}*/
                    }

                    .project-motto {
                        width: 160px;
                        font-size: 18px;
                        color: $secondaryFontColor;
                        z-index: 1;
                        font-family: DeathStar, sans-serif;
                        letter-spacing: 8px;
                        margin: 20px 0 0 320px;

                        /*
                                font-size: 21px;
                        color: $secondaryFontColor;
                        z-index: 1;
                        font-family: DeathStar, sans-serif;
                        letter-spacing: 12px;
                        margin: 20px 0 0 250px;

                         */

                    }

                    .moveOn-link {
                        font-size: 15px;
                        font-family: Nunitoregular, sans-serif;
                        color: white;
                        z-index: 1;
                        margin: 260px 0 0 320px;
                        padding-top: 15px;
                        transition: text-shadow .3s;
                        border-top: 2px solid $mainLightColor;

                        /**
                               font-size: 18px;
                        font-family: Nunitoregular, sans-serif;
                        color: white;
                        z-index: 1;
                        margin: 30px 0 0 250px;
                        padding-top: 30px;
                        transition: text-shadow .3s;
                        border-top: 2px solid $mainLightColor;
                         */

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
                background: url("../assets/images/header/city-bcg-photo.png") -895px  -415px;
                -webkit-text-fill-color: rgba(255, 66, 0, .5);
                -webkit-background-clip: text;
                font-size: 320px;
                font-family: DeathStar, sans-serif;


               /* @media screen and (min-width: 1920px) {
                    background: url("../assets/images/header/city-bcg-photo.png") -743px  -155px;
                }*/

            }
        }

        .center-big-letter {
            font-size: 720px;
            color: #ff4200;
            opacity: .5;
        }
    }

</style>
