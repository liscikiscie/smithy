<template>
    <div id="app">
        <header>
            <div class="logo">SMITHY</div>
            <nav>
                <div class="nav-container">
                    <div class="nav-operators">
                        <font-awesome
                                class="nav-icon hamburger"
                                icon="bars"
                                v-if="navState===false"
                                @click="toggleNav"
                                key="open"/>
                        <font-awesome
                                class="nav-icon closing"
                                icon="times"
                                @click="toggleNav"
                                v-else
                                key="closed"/>
                    </div>
                    <div class="nav">
                        <transition-group
                                name="stagger"
                                tag="ul"
                                class="navigation-list"
                                v-if="navState"
                        >
                            <li v-for="route in this.$router.options.routes" :key="route.name">
                                <router-link :to="route.path">{{ route.name }}</router-link>
                            </li>
                        </transition-group>
                    </div>
                    <router-view/>
                </div>
            </nav>
        </header>
    </div>
</template>

<script>
    export default {
        name: 'App',
        data() {
            return {
                navState: false
            }
        },
        methods: {
            toggleNav() {
                this.navState = !this.navState;
            }
        }
    }
</script>

<style lang="scss">
    @import "./scss/main";
    @import "./scss/typography/deathStar";

    #app {
        text-align: center;
        position: relative;
    }

    .logo {
        position: absolute;
        top: 29px;
        left: 40px;
        z-index: 100;
        font-family: 'DeathStar', sans-serif;
        font-weight: bold;
        font-size: 22px;
        color: #ffffff;
        cursor: default;
        user-select: none;

        @media screen and (min-width: 767px) {
            font-size: 36px;
        }
    }

    .nav-container {
        position: fixed;
        display: flex;
        justify-content: flex-end;
        flex-flow: row;
        user-select: none;

        .nav-operators {
            position: fixed;
            top: 25px;
            right: 28px;
            font-size: 26px;
            z-index: 100;

            @media screen and (min-width: 320px) {
                font-size: 22px;
            }

            @media screen and (min-width: 767px) {
                font-size: 28px;
            }

            .nav-icon {
                cursor: pointer;
                padding: 5px;
                color: $secondaryFontColor;
                z-index: 100;

            }

            &:hover {
                animation: pulse 1s linear infinite;

            }

            @keyframes pulse {
                0% {
                    transform: scale(1);
                }
                50% {
                    transform: scale(1.1);
                }
                100% {
                    transform: scale(1);
                }
            }
        }

        .closing-menu {
            font-size: 32px;
        }

        .nav {
            position: fixed;
            top: 60px;
            right: 0;
            z-index: 100;

            @media screen and (min-width: 767px) {
                position: fixed;
                top: 30px;
                right: 75px;
                z-index: 100;
            }


            .navigation-list {
                display: flex;
                justify-content: flex-end;
                flex-direction: column;

                @media screen and (min-width: 767px) {
                    flex-direction: row;
                }

                li {
                    margin-top: 15px;

                    @media screen and (min-width: 767px) {
                        margin-top: 3px;
                    }
                }

            }

            a {
                font-weight: bold;
                color: $secondaryFontColor;
                font-size: 15px;
                text-decoration: none;
                margin: 0 12px;

                @media screen and (min-width: 767px) {
                    font-size: 18px;
                }

                &.router-link-exact-active {
                    color: $mainLightColor;
                }
            }
        }
    }
</style>
