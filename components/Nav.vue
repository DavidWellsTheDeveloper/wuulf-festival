<template>
    <v-container grid-list-xs>
        <v-app-bar dense fixed color="#1d467" dark>
            <v-toolbar-title v-text="title" />
            <v-spacer></v-spacer>
            <div v-for="item in items" :key="item.to">
                <v-btn v-if="onHomePage && item.homeItem" text color="green" @click="$vuetify.goTo(item.to, scrollOptions)">
                    {{ item.title }}
                </v-btn>

                <v-btn v-else text type="link" color="green" :href="'/' + item.to">
                {{ item.title }}
            </v-btn>
            </div>
            
        </v-app-bar>
    </v-container>
</template>

<script>
    export default {
        data() {
            return {
                items: [
                    {
                        icon: 'mdi-apps',
                        title: 'Home',
                        to: '#welcome',
                        homeItem: true
                    },
                    {
                        title: 'WUULF 2023',
                        to: '#wuulf2023',
                        homeItem: true
                    },
                    {
                        icon: 'mdi-chart-bubble',
                        title: 'Calendar',
                        to: '#calendar',
                        homeItem: true
                    },
                    {
                        icon: 'mdi-chart-bubble',
                        title: 'Registration',
                        to: '#registration',
                        homeItem: true
                    },
                    // {
                    //     icon: 'mdi-chart-bubble',
                    //     title: 'Past WUULF\'s',
                    //     to: 'pastWuulfs',
                    //     homeItem: false
                    // }
                ],
                scrollOptions: {
                    offset: 100,
                    duration: 800,
                },
                title: "WUULF",
            }
        },
        computed: {
            onHomePage() {
                return this.$route.path === "/" 
            }
        },
    }
</script>

<style lang="scss" scoped>

</style>