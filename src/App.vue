<template>
    <div id="app">
        <div class="logo">SMITHY</div>
        <div class="nav-container">
            <div class="nav-operators">
                <font-awesome
                        class="nav-icon hamburger-menu"
                        icon="bars"
                        v-if="navState===false"
                        @click="toggleNav"
                        key="open"/>
                <font-awesome
                        class="nav-icon closing-menu"
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
                        <router-link :to="route.path" >{{ route.name }}</router-link>
                    </li>
                </transition-group>
            </div>
            <router-view/>
        </div>
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
            },
            // beforeEnter( el ) {
            //     el.style.opacity = 0;
            //     el.style.height = 0;
            // }
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
        font-size: 42px;
        color: $secondaryFontColor;
    }

    .nav-container {
        position: fixed;
        display: flex;
        justify-content: flex-end;
        flex-flow: row;

        .nav-operators {
            position: fixed;
            top: 25px;
            right: 28px;
            font-size: 26px;
            z-index: 100;

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
            top: 30px;
            right: 75px;
            z-index: 100;

            .navigation-list {
                display: flex;
                justify-content: flex-end;
                flex-direction: row;
            }

            a {
                font-weight: bold;
                color: $secondaryFontColor;
                font-size: 26px;
                text-decoration: none;
                margin: 0 12px;

                &.router-link-exact-active {
                    color: $mainLightColor;
                }
            }
        }
    }
</style>
