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
            bottom: 0;
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
                align-items: center;

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
            display: flex;
            justify-content: center;
            align-items: center;

            .project-description {
                display: flex;
                justify-content: center;
                align-items: center;
                cursor: default;
                user-select: none;
                z-index: 2;

                .description-wrapper {
                    display: flex;
                    flex-direction: column;
                    height: 350px;
                    margin-top: 10px;

                    @media (max-width: 568px) and (min-width: 320px) {
                        height: 100px;
                    }

                    @media screen and (min-width: 767px) {
                        height: 400px;
                    }

                    .project-name {
                        display: none;

                        @media screen and (min-width: 767px) {
                            display: flex;
                            font-size: 32px;
                            color: white;
                            z-index: 1;
                            font-family: DeathStar, sans-serif;
                            letter-spacing: 20px;
                            margin: 100px 0 0 20px;
                        }
                    }
                }

                .project-motto {
                    width: 160px;
                    font-size: 18px;
                    color: $secondaryFontColor;
                    z-index: 1;
                    font-family: DeathStar, sans-serif;
                    letter-spacing: 8px;
                    padding-bottom: 250px;

                    @media (max-width: 568px) and (min-width: 320px) {
                        padding-bottom: 130px;
                    }

                    @media screen and (min-width: 567px) {
                        white-space: nowrap;
                        font-size: 14px;
                        display: flex;
                        justify-content: center;

                    }

                    @media screen and (min-width: 767px) {
                        margin-left: 46px;
                        display: flex;
                        justify-content: center;
                        margin-top: 100px;
                        white-space: nowrap;
                        font-size: 18px;
                    }

                    /*margin: 20px 0 0 320px;
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
                    padding-top: 15px;
                    transition: text-shadow .3s;
                    border-top: 2px solid $mainLightColor;

                    @media screen and (min-width: 567px) {
                        margin: 0;
                    }

                    @media screen and (min-width: 767px) {
                        margin-top: -59px;
                    }

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

        @media screen and (min-width: 767px) {

        }

        .letter-orange {
            background-image: url("../assets/images/header/city-bcg-photo.png");
            background-repeat: no-repeat;
            background-position: 0 0;
            background-size: 320px 568px;
            -webkit-text-fill-color: rgba(255, 66, 0, .5);
            -webkit-background-clip: text;
            font-size: 320px;
            font-family: DeathStar, sans-serif;

            @media screen and (min-width: 567px) {
                font-size: 200px;
            }

            @media screen and (min-width: 767px) {
                font-size: 480px;
                background-image: url("../assets/images/header/city-bcg-photo.png");
                background-size: 768px 1024px;
                background-repeat: no-repeat;
                background-position: 0px 0px;
            }

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

</style>
