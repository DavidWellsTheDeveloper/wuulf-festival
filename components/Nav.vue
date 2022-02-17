<template>
    <v-container grid-list-xs>
        <v-app-bar dense fixed color="#1d467" dark>
            <v-toolbar-title v-text="title" />
            <v-spacer></v-spacer>
            <v-btn text color="green" v-for="item in items" @click="$vuetify.goTo(item.to, scrollOptions)" :key="item.to">
                {{ item.title }}
            </v-btn>
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
                        to: '#welcome'
                    },
                    {
                        icon: 'mdi-chart-bubble',
                        title: 'Calendar',
                        to: '#calendar'
                    },
                    {
                        icon: 'mdi-chart-bubble',
                        title: 'Registration',
                        to: '#registration'
                    }
                ],
                scrollOptions: {
                    offset: 100
                },
                title: "WUULF",
            }
        },
    }
</script>

<style lang="scss" scoped>

</style>