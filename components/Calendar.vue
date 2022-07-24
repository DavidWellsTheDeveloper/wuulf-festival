<template>
  <v-container id="calendar" fluid class="p-5">
    <v-row align="center">
      <iframe src="https://calendar.google.com/calendar/embed?src=ff3f7k1mpekg07ubdq3a4paaks%40group.calendar.google.com&ctz=America%2FDenver" style="border: 0; margin: auto;" width="80%" height="800" frameborder="0" scrolling="no"></iframe>
    </v-row>
  </v-container>
</template>

<script>
import {default as events} from '../static/activities_2022.js'
  export default {
    name: 'WuulfCalendar',
    data() {
      return {
        value: '2022-06-20 13:00',
        weekday: [1, 2, 3, 4, 5, 6, 0],
        type: 'day',
        types: ['week', 'day'],
        selectedEvent: {},
        selectedElement: null,
        selectedOpen: false,
        events: events,
        eventColors: [
          {
            eventType: 'Meal',
            color: 'purple'
          },
          {
            eventType: 'Community',
            color: 'green darken-1'
          },
          {
            eventType: 'Early Risers',
            color: 'pink darken-1'
          },
          {
            eventType: 'Activity',
            color: 'orange accent-3'
          },
          {
            eventType: 'Ghost Ranch Activity',
            color: 'blue'
          },
          {
            eventType: 'Youth Programming',
            color: 'teal'
          },
        ]

      }
    },
    computed: {
      selectedDate() {
        return (this.$refs.calendar) ? this.$refs.calendar.title : '' 
      }
    },
    methods: {
      setToday() {
        this.value = ''
      },
      jumpToWuulf() {
        this.value = '2022-06-20 13:00'
      },
      showEvent ({ nativeEvent, event }) {
        const open = () => {
          this.selectedEvent = event
          this.selectedElement = nativeEvent.target
          requestAnimationFrame(() => requestAnimationFrame(() => this.selectedOpen = true))
        }

        if (this.selectedOpen) {
          this.selectedOpen = false
          requestAnimationFrame(() => requestAnimationFrame(() => open()))
        } else {
          open()
        }

        nativeEvent.stopPropagation()
      },
      getEventColor(event) {
        // default color is black
        var color = 'black'
        this.eventColors.forEach(element => {
          if (event.type == element.eventType){
            color = element.color
          }
        })
        return color
      }

    },
  }
</script>

<style lang="scss" scoped>

</style>