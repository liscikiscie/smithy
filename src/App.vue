<template>
    <div id="app">
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
        <div class="nav">
            <router-link to="/" key="home">Home</router-link>
            |
            <router-link to="/about" key="about">About</router-link>
            |
            <router-link to="/services" key="services">Services</router-link>
            |
            <router-link to="/portfolio" key="portfolio">Portfolio</router-link>
            |
            <router-link to="/contact" key="contact">Contact</router-link>
        </div>
        <router-view/>
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

    #app {
        font-family: 'Avenir', Helvetica, Arial, sans-serif;
        text-align: center;
        position: relative;
    }

    .nav-icon {
        position: absolute;

        cursor: pointer;
        padding: 5px;

        &:hover {
            animation: pulse 1s linear infinite;

        }

        @keyframes pulse {
            0% {
                transform: scale(1);
            }
            50% {
                transform: scale(1.2);
            }
            100% {
                transform: scale(1);
            }
        }
    }

    .hamburger-menu {
        font-size: 26px;
        top: 29px;
        right: 40px;
    }

    .closing-menu {
        font-size: 34px;
        top: 29px;
        right: 40px;
    }

    .nav {
        padding: 30px;
        display: none;

        a {
            font-weight: bold;
            color: #2c3e50;

            &.router-link-exact-active {
                color: #42b983;
            }
        }
    }
</style>
