<template>
  <v-container id="calendar" fluid class="p-5">
    <v-row align="center">
      <iframe src="https://calendar.google.com/calendar/embed?src=ff3f7k1mpekg07ubdq3a4paaks%40group.calendar.google.com&ctz=America%2FDenver" style="border: 0; margin: auto;" width="80%" height="800" frameborder="0" scrolling="no"></iframe>
    </v-row>
  </v-container>
</template>

<script>
  export default {
    name: 'WuulfCalendar',
    data() {
      return {
      }
    },
    computed: {
    },
    methods: {
    },
  }
</script>

<style lang="scss" scoped>

</style>