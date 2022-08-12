<template>
    <v-container grid-list-xs>
        <h1>Past WUULF's</h1>
        <p>As an intergenerational camp, it's inspiring to know that WUULF has been around long enough to see generations grow from children to adults at WUULF year after year.</p>
        <v-timeline>
            <v-timeline-item
                v-for="(event, i) in events"
                :key="i"
                :color="event.color"
                small
                >
                <template v-slot:opposite>
                    <span
                    :class="`headline font-weight-bold ${event.color}--text`"
                    v-text="event.year"
                    ></span>
                </template>
                <v-card class="elevation-2">
                    <v-card-title class="text-h5">
                    {{ event.title }}
                    </v-card-title>
                    <v-card-text>
                    {{ event.text }}
                    </v-card-text>
                </v-card>
                </v-timeline-item>
        </v-timeline>
        <h2>Photos</h2>

    </v-container>
</template>

<script>
    export default {
        name: "pastWuulfs",
        data() {
            return {
                events: [
                    {
                    title: 'A few UU Families visit Ghost Ranch',
                    text: 'In it\'s humble beginings, a few UU families attended Ghost Ranch together, and an annual tradition to continue visiting year after year.',
                    color: 'secondary',
                    year: '1960',
                    },
                    {
                    title: 'The group took on the name "Mountain Desert Family Festival".',
                    text: '',
                    color: 'accent',
                    year: 'Unknow',
                    },
                    {
                    title: 'Mountain Desert Family Festival became a non-profit',
                    text: 'Claudia Van Buren was president of the Mountain Desert Family Festival, and applied the organization for 501c non-profit status. This was a big step towards making us the organization it is today.',
                    color: 'priary',
                    year: '1996',
                    },
                    {
                    title: 'Event 1',
                    text: 'Lorem Ibsem asdfj we ew vd adsf.',
                    color: 'info',
                    year: '1990',
                    },
                    {
                    title: 'Event 1',
                    text: 'Lorem Ibsem asdfj we ew vd adsf.',
                    color: 'warning',
                    year: '2000',
                    },
                ],
            }
        },
    }
</script>

<style lang="scss" scoped>

</style>