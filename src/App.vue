<template>
    <v-app>

        <v-content app>
            <v-container fluid>
                <router-view></router-view>
            </v-container>
        </v-content>
    </v-app>
</template>

<script>

    export default {
        components: {},
        computed: {
            currentUser() {
                return this.$store.state.auth.user;
            },
            hide() {
                return this.$route.path === '/login' || this.$route.path === '/register';
            }
        }
    }
</script>

<style>

    #app {
        margin: 0;
        padding: 0;
        background-color: #252a41;
        font-family: 'Helvetica', 'RobotoDraft', 'Roboto', sans-serif;
        font-size: 14px;
        -webkit-font-smoothing: antialiased;
        -moz-osx-font-smoothing: grayscale;
    }


</style>
