<template>
        <nav>
            <v-toolbar class="light-blue accent-1" app height="100px">
                <v-container>
                    <v-row justify="center">
                        <v-toolbar-title >
                            <h1>Kontura Projekt D.O.O.</h1>
                        </v-toolbar-title>
                    </v-row>
                    <v-row justify="center">

                    <v-layout display="flex-row-reverse">

                            <v-toolbar-item>
                                <v-btn flat rounded color="amber lignten-3">
                                    <router-link to="/">HOME</router-link>
                                </v-btn>
                                <v-btn flat rounded color="amber lignten-3">
                                    <router-link to="/about">ABOUT</router-link>
                                </v-btn>
                                <v-btn flat rounded color="amber lignten-3">
                                    <router-link to="/buildings">BUILDINGS</router-link>
                                </v-btn>
                                <v-btn flat rounded color="amber lignten-3">
                                    <router-link to="/contact">CONTACT</router-link>
                                </v-btn>
                                <v-btn flat rounded color="amber lignten-3">
                                    <router-link to="/log">LOG IN/REGISTER</router-link>
                                </v-btn>
                            </v-toolbar-item>

                    </v-layout>

                    </v-row>
                </v-container>
            </v-toolbar>
        </nav>
</template>


<script>
export default {
    data() {
        return {
            links: [
                { text: 'Home', route: '/' },
                { text: 'About', route: '/about' },
                { text: 'Buildings', route: '/buildings' },
                { text: 'Contact', route: '/contact' },
                { text: 'Log in', route: '/log'}
            ]
        }
    }
}
</script>