<template>
  <v-container id="calendar" fluid class="p-5">
    <v-row align="center">
      <iframe src="https://calendar.google.com/calendar/embed?src=ff3f7k1mpekg07ubdq3a4paaks%40group.calendar.google.com&ctz=America%2FDenver" style="border: 0; margin: auto;" width="80%" height="600" frameborder="0" scrolling="no"></iframe>
    </v-row>
    <!-- <v-row>
      <v-col>
        <h4 class="text-center">Schedule Subject to Change</h4>
      </v-col>
    </v-row>
    <v-row justify="center">
      <v-col cols="11" lg="3">
        <v-btn
          outlined
          class="mr-4"
          color="green"
          @click="jumpToWuulf"
        >
          Jump To WUULF Week
        </v-btn>

        <v-btn
          outlined
          class=""
          color="green"
          @click="setToday"
        >
          Today
        </v-btn>
      </v-col>
      <v-col cols="11" lg="8">
        <v-select
          v-model="type"
          :items="types"
          dense
          outlined
          hide-details
          class="ma-2"
          label="calendar type"
        ></v-select>
      </v-col>
    </v-row>
    <v-row justify="center">
      <v-col cols="11">
        <v-btn
          icon
          @click="$refs.calendar.prev()"
        >
          <v-icon>mdi-chevron-left</v-icon>
        </v-btn>
        <v-btn
          icon
          @click="$refs.calendar.next()"
        >
          <v-icon>mdi-chevron-right</v-icon>
        </v-btn>
        <p v-if="$refs.calendar">{{ $refs.calendar.title }}</p>
      </v-col>
    </v-row>
    <v-row justify="center" align="center">
      <v-col cols="11">
        <v-sheet height="850">
        <v-calendar
          ref="calendar"
          first-interval="6"
          @click:event="showEvent"
          v-model="value"
          :weekdays="weekday"
          :type="type"
          :events="events"
          event-overlap-mode="stack"
          :event-color="getEventColor"
        ></v-calendar>
        <v-menu
          v-model="selectedOpen"
          :close-on-content-click="false"
          :activator="selectedElement"
          offset-x
        >
          <v-card
            color="grey lighten-4"
            flat
          >
            <v-toolbar
              :color="selectedEvent.color"
              dark
            >
              <v-toolbar-title v-html="selectedEvent.name"></v-toolbar-title>
              <v-spacer></v-spacer>
              {{ selectedEvent.type }}
            </v-toolbar>
            <v-card-text>
              <span style="color: black;">{{ selectedEvent.description }}</span>
            </v-card-text>
            <v-card-actions>
              <v-btn
                text
                color="secondary"
                @click="selectedOpen = false"
              >
                Cancel
              </v-btn>
            </v-card-actions>
          </v-card>
        </v-menu>
        </v-sheet>
      </v-col>
    </v-row>
    <v-row justify="center">
      <v-col cols="12" md="8" lg="6">
        <v-card>
          <v-card-title>Calendar Legend</v-card-title>
          <v-card-text>
            <v-chip v-for="item in eventColors" :color="item.color" :key="item.eventType">
                {{ item.eventType }}
            </v-chip>
          </v-card-text>
        </v-card>
      </v-col>
    </v-row> -->
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