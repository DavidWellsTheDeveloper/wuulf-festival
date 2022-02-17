<template>
  <v-container id="calendar">
    <v-row>
      <v-toolbar
          flat
        >
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
      <v-toolbar-title v-if="$refs.calendar">
        {{ selectedDate }}
      </v-toolbar-title>
      <v-spacer></v-spacer>
      <v-select
        v-model="type"
        :items="types"
        dense
        outlined
        hide-details
        class="ma-2"
        label="calendar type"
      ></v-select>
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
      </v-toolbar>
    </v-row>
    <v-row justify="center" align="center">
      <v-col cols="12">
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
            min-width="450px"
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
          <v-card-title>Legend</v-card-title>
          <v-card-text>
            <v-chip v-for="item in eventColors" :color="item.color" :key="item.eventType">
                {{ item.eventType }}
            </v-chip>
          </v-card-text>
        </v-card>
      </v-col>
    </v-row>
  </v-container>
</template>

<script>
  export default {
    name: 'WuulfCalendar',
    data() {
      return {
        value: '2022-06-20 13:00',
        weekday: [1, 2, 3, 4, 5, 6, 0],
        type: 'week',
        types: ['week', 'day'],
        selectedEvent: {},
        selectedElement: null,
        selectedOpen: false,
        events: [
          {
            name: 'Check In',
            start: '2022-06-20 15:00',
            end: '2022-06-20 17:00',
            type: 'Community',
            description: 'Meet at the Lower Pavilion to begin the week. Here you will get essential information about the weeks activities & expectations.'
          },
          {
            name: 'Ghost Ranch Tour for New WUULFies',
            start: '2022-06-20 17:00',
            end: '2022-06-20 17:30',
            type: 'Ghost Ranch Activity',
            description: 'New to WUULF? '
          },
          {
            name: 'Dinner',
            start: '2022-06-20 17:30',
            end: '2022-06-20 19:00',
            type: 'Meal',
            description: 'Meals are provided at the Dining Hall. Please remember to bring your name tag. Dietary options available.'
          },
          {
            name: 'Orientation & Late Registration',
            start: '2022-06-20 19:00',
            end: '2022-06-20 21:00',
            type: 'Community',
            description: 'If you haven\'t registered yet, this is you\'re last chance.'
          },
          {
            name: 'Music & Sing-a-long',
            start: '2022-06-20 21:00',
            end: '2022-06-20 22:00',
            type: 'Activity',
            description: 'Participants are invited to bring their acoustic instruments: guitars, fiddles, banjos, etc. and of course your singing voice! If you have a copy of "Rise Up Singing" (which is an awesome sing-a-long songbook) please bring it and we\'ll make music in the evening before retiring at 10:00 pm (Ghost Ranch Quiet Time).'          },
          {
            name: 'Ghost Ranch Quiet Hours Begin',
            start: '2022-06-20 22:00',
            end: '2022-06-20 23:00',
            type: 'Ghost Ranch Activity',
            description: 'Ghost ranch hosts other events, groups, and staff on site. Please be respectful of others, and keep evening activities at a low decibel. In addition, WUULFies (under 18) must be in their rooms by the time quiet hours begin.'
          },

          {
            name: 'Breakfast',
            start: '2022-06-21 7:30',
            end: '2022-06-21 8:00',
            type: 'Meal',
            description: 'Meals are provided at the Dining Hall. Please remember to bring your name tag. Dietary options available.'
          },
          {
            name: 'Community Gathering',
            start: '2022-06-21 8:15',
            end: '2022-06-21 9:00',
            type: 'Community',
            description: 'While at ghost ranch, the community minister will hold a daily kid friendly service by the big tree which usually includes a short sermon and singing.'
          },
          {
            name: 'Program Day',
            start: '2022-06-21 9:00',
            end: '2022-06-21 16:30',
            type: 'Youth Programming',
            description: ''
          },
          
          {
            name: 'Lunch',
            start: '2022-06-21 12:00',
            end: '2022-06-21 13:00',
            type: 'Meal',
            description: 'Meals are provided at the Dining Hall. Please remember to bring your name tag. Dietary options available.'
          },
          {
            name: 'Swim',
            start: '2022-06-21 13:00',
            end: '2022-06-21 16:30',
            type: 'Activity',
            description: 'Visit the pool for a cool way to beat the heat after lunch. Note that kids must be with a responsible adult while at the pool.'
          },
          {
            name: 'Craft: Water Colors w/ Rick Wells',
            start: '2022-06-21 13:00',
            end: '2022-06-21 14:30',
            type: 'Activity',
            description: 'Capture the natural beauty of the Ghost Ranch!  Rick will lead a class in water color technique suitable for beginners and more experienced painters.'
          },
          {
            name: 'Talk: Braiding Sweetgrass w/ Jane Everham',
            start: '2022-06-21 14:30',
            end: '2022-06-21 16:30',
            type: 'Activity',
            description: 'Drawing on her life as an indigenous scientist, and as a woman, Kimmerer shows how other living beings―asters and goldenrod, strawberries and squash, salamanders, algae, and sweetgrass―teaches lessons.  The book argues that the awakening of ecological consciousness requires the acknowledgment and celebration of our reciprocal relationship.'
          },
          {
            name: 'Happy Hour & Community Time',
            start: '2022-06-21 16:30',
            end: '2022-06-21 17:30',
            type: 'Community',
            description: 'Come visit with friends at the Lower Pavilian to play yard games, enjoy music, and hang out. There will be snacks and drinks (adult beverages & non-alcoholic beverages available).'          },
          {
            name: 'Dinner',
            start: '2022-06-21 17:30',
            end: '2022-06-21 19:00',
            type: 'Meal',
            description: 'Meals are provided at the Dining Hall. Please remember to bring your name tag. Dietary options available.'
          },
          {
            name: 'Game Night/Festival of Friends Old and New',
            start: '2022-06-21 19:00',
            end: '2022-06-21 21:00',
            type: 'Community',
            description: 'Music, games, conversation and community. Let\'s celebrate together! Wine and beer will be provided.'
          },
          {
            name: 'Music & Sing-a-long',
            start: '2022-06-21 21:00',
            end: '2022-06-21 22:00',
            type: 'Activity',
            description: 'Participants are invited to bring their acoustic instruments: guitars, fiddles, banjos, etc. and of course your singing voice! If you have a copy of "Rise Up Singing" (which is an awesome sing-a-long songbook) please bring it and we\'ll make music in the evening before retiring at 10:00 pm (Ghost Ranch Quiet Time).'          },
          {
            name: 'Ghost Ranch Quiet Hours',
            start: '2022-06-21 22:00',
            end: '2022-06-21 23:00',
            type: 'Ghost Ranch Activity',
            description: 'Ghost ranch hosts other events, groups, and staff on site. Please be respectful of others, and keep evening activities at a low decibel. In addition, WUULFies (under 18) must be in their rooms by the time quiet hours begin.'          },

          {
            name: 'Breakfast',
            start: '2022-06-22 7:30',
            end: '2022-06-22 8:00',
            type: 'Meal',
            description: 'Meals are provided at the Dining Hall. Please remember to bring your name tag. Dietary options available.'
          },
          {
            name: 'Community Gathering',
            start: '2022-06-22 8:15',
            end: '2022-06-22 9:00',
            type: 'Community',
            description: 'While at ghost ranch, the community minister will hold a daily kid friendly service by the big tree which usually includes a short sermon and singing.'
          },
          {
            name: 'Offsite',
            start: '2022-06-22 9:00',
            end: '2022-06-22 12:00',
            type: 'Activity',
            description: ''
          },
          {
            name: 'Shamshoian, Armenian Line Dance',
            start: '2022-06-22 9:00',
            end: '2022-06-22 10:30',
            type: 'Activity',
            description: 'Susan and Kimberly Shamshoian-Sakamoto will teach some basic and fun Armenian line dances set to traditional music.'
          },
          {
            name: 'Talk: Book Club',
            start: '2022-06-22 10:30',
            end: '2022-06-22 12:00',
            type: 'Activity',
            description: ''
          },
          {
            name: 'Hike: TBD',
            start: '2022-06-22 9:00',
            end: '2022-06-22 12:00',
            type: 'Activity',
            description: 'Meet at the Lower Pavilion to join in for a morning hike.'
          },
          {
            name: 'Lunch',
            start: '2022-06-22 12:00',
            end: '2022-06-22 13:00',
            type: 'Meal',
            description: 'Meals are provided at the Dining Hall. Please remember to bring your name tag. Dietary options available.'
          },
          {
            name: 'Swim',
            start: '2022-06-22 13:00',
            end: '2022-06-22 16:30',
            type: 'Activity',
            description: 'Visit the pool for a cool way to beat the heat after lunch. Note that kids must be with a responsible adult while at the pool.'
          },
          {
            name: 'Craft: Jewelry w/ Peggy',
            start: '2022-06-22 13:00',
            end: '2022-06-22 14:30',
            type: 'Activity',
            description: 'Peggy will bring supplies for jewelry making, focusing on amazing dangly earrings!  Make a pair for yourself, your mom, or a favorite WUULF friend!'
          },
          {
            name: 'Talk: Reser, Climate',
            start: '2022-06-22 14:30',
            end: '2022-06-22 16:30',
            type: 'Activity',
            description: 'This discussion-based workshop will dive into the ever-important topic of climate change and environmental sustainability. We will cover the basics, internalize the magnitude of the impacts, and develop local action plans to create a healthy, happy future for the interdependent web of all existence. BONUS: Come learn about WUULF and Ghost Ranch\'s sustainability initiatives, and how you can participate.'
          },
          {
            name: 'Henna under tree',
            start: '2022-06-22 13:00',
            end: '2022-06-22 14:30',
            type: 'Activity',
            description: 'Meet under the big tree for some henna.'
          },
          {
            name: 'Happy Hour & Community Time',
            start: '2022-06-22 16:30',
            end: '2022-06-22 17:30',
            type: 'Community',
            description: 'Come visit with friends at the Lower Pavilian to play yard games, enjoy music, and hang out. There will be snacks and drinks (adult beverages & non-alcoholic beverages available).'          },
          {
            name: 'Dinner',
            start: '2022-06-22 17:30',
            end: '2022-06-22 19:00',
            type: 'Meal',
            description: 'Meals are provided at the Dining Hall. Please remember to bring your name tag. Dietary options available.'
          },
          {
            name: 'Solstice Service',
            start: '2022-06-22 19:00',
            end: '2022-06-22 21:00',
            type: 'Community',
            description: 'Solstice Celebration - Join us for an inspirational multigenerational event. Celebrate the changing of the season with a musical sunset solstice ritual with chants, drumming, dancing, and other sacred rhythms shared at Echo Amphitheater, a special place inside Mother Earth. All instruments welcome but remember that you need to carry your stuff up the hill and several flights of stairs! Brawny people will be recruited as necessary to help carry those unable to make the hike. Echo Amphitheater is about a ten-minute drive from Ghost Ranch. Remember to bring your flashlights, jackets and bug repellent.'
          },
          {
            name: 'Music & Sing-a-long',
            start: '2022-06-22 21:00',
            end: '2022-06-22 22:00',
            type: 'Activity',
            description: 'Participants are invited to bring their acoustic instruments: guitars, fiddles, banjos, etc. and of course your singing voice! If you have a copy of "Rise Up Singing" (which is an awesome sing-a-long songbook) please bring it and we\'ll make music in the evening before retiring at 10:00 pm (Ghost Ranch Quiet Time).'          },
          {
            name: 'Ghost Ranch Quiet Hours',
            start: '2022-06-22 22:00',
            end: '2022-06-22 23:00',
            type: 'Ghost Ranch Activity',
            description: 'Ghost ranch hosts other events, groups, and staff on site. Please be respectful of others, and keep evening activities at a low decibel. In addition, WUULFies (under 18) must be in their rooms by the time quiet hours begin.'          },

          {
            name: 'Breakfast',
            start: '2022-06-23 7:30',
            end: '2022-06-23 8:00',
            type: 'Meal',
            description: 'Meals are provided at the Dining Hall. Please remember to bring your name tag. Dietary options available.'
          },
          {
            name: 'Community Gathering',
            start: '2022-06-23 8:15',
            end: '2022-06-23 9:00',
            type: 'Community',
            description: 'While at ghost ranch, the community minister will hold a daily kid friendly service by the big tree which usually includes a short sermon and singing.'
          },
          {
            name: 'Program Day',
            start: '2022-06-23 9:00',
            end: '2022-06-23 16:30',
            type: 'Youth Programming',
            description: ''
          },
          {
            name: 'Lunch',
            start: '2022-06-23 12:00',
            end: '2022-06-23 13:00',
            type: 'Meal',
            description: 'Meals are provided at the Dining Hall. Please remember to bring your name tag. Dietary options available.'
          },
          {
            name: 'Swim',
            start: '2022-06-23 13:00',
            end: '2022-06-23 16:30',
            type: 'Activity',
            description: 'Visit the pool for a cool way to beat the heat after lunch. Note that kids must be with a responsible adult while at the pool.'
          },
          {
            name: 'Craft: Tie Dye',
            start: '2022-06-23 13:00',
            end: '2022-06-23 14:30',
            type: 'Activity',
            description: 'Join us for a very fun tie dye workshop. Please bring with you any 100% co􀆩on, 100% rayon or 100% silk pieces you would like to dye. These can be t-shirts, skirts, pants, scarves, sheets, underwear, socks and countless other items. Your creativity is DYEING to come out.'
          },
          {
            name: 'Talk: Eldredge, Ageism',
            start: '2022-06-23 14:30',
            end: '2022-06-23 16:30',
            type: 'Activity',
            description: 'Ageism involves discriminating against someone because of their age. Ageism can appear in either subtle or overt forms everyday life. Most people over 50 have experienced this form of discrimination. Ageism in the workplace is illegal. It still happens despite the protections of Federal laws. Ageism hurts not only those over 50. It hurts their loved ones, their co-workers, and their workplaces. In this two-hour workshop, we will first identify the many forms of nuanced ageism. We then will review the laws intended to protect older Americans. Finally, we will cover strategies to counter these many forms of discrimination.'
          },
          {
            name: 'Happy Hour & Community Time',
            start: '2022-06-23 16:30',
            end: '2022-06-23 17:30',
            type: 'Community',
            description: 'Come visit with friends at the Lower Pavilian to play yard games, enjoy music, and hang out. There will be snacks and drinks (adult beverages & non-alcoholic beverages available).'          },
          {
            name: 'Dinner',
            start: '2022-06-23 17:30',
            end: '2022-06-23 19:00',
            type: 'Meal',
            description: 'Meals are provided at the Dining Hall. Please remember to bring your name tag. Dietary options available.'
          },
          {
            name: 'Karaoke Night',
            start: '2022-06-23 19:00',
            end: '2022-06-23 21:00',
            type: 'Community',
            description: 'Bring your best, worst, or silliest singing voices! Everyone is invited to listen, sing, and laugh as we let go of our inhibitions and let our inner musicians out.  This is a low pressure “group sing” style karaoke where all types of music and abilities are appreciated!'
          },
          {
            name: 'Music & Sing-a-long',
            start: '2022-06-23 21:00',
            end: '2022-06-23 22:00',
            type: 'Activity',
            description: 'Participants are invited to bring their acoustic instruments: guitars, fiddles, banjos, etc. and of course your singing voice! If you have a copy of "Rise Up Singing" (which is an awesome sing-a-long songbook) please bring it and we\'ll make music in the evening before retiring at 10:00 pm (Ghost Ranch Quiet Time).'          },
          {
            name: 'Ghost Ranch Quiet Hours',
            start: '2022-06-23 22:00',
            end: '2022-06-23 23:00',
            type: 'Ghost Ranch Activity',
            description: 'Ghost ranch hosts other events, groups, and staff on site. Please be respectful of others, and keep evening activities at a low decibel. In addition, WUULFies (under 18) must be in their rooms by the time quiet hours begin.'          },

          {
            name: 'Breakfast',
            start: '2022-06-24 7:30',
            end: '2022-06-24 8:00',
            type: 'Meal',
            description: 'Meals are provided at the Dining Hall. Please remember to bring your name tag. Dietary options available.'
          },
          {
            name: 'Community Gathering',
            start: '2022-06-24 8:15',
            end: '2022-06-24 9:00',
            type: 'Community',
            description: 'While at ghost ranch, the community minister will hold a daily kid friendly service by the big tree which usually includes a short sermon and singing.'
          },
          {
            name: 'Offsite',
            start: '2022-06-24 9:00',
            end: '2022-06-24 12:00',
            type: 'Activity',
            description: ''
          },
          {
            name: 'Talk: TBD',
            start: '2022-06-24 10:30',
            end: '2022-06-24 12:00',
            type: 'Activity',
            description: ''
          },
          {
            name: 'Labrynth Walk w/ Jane Everham',
            start: '2022-06-24 9:00',
            end: '2022-06-24 10:30',
            type: 'Activity',
            description: 'Stroll up to the Labyrinth for a quiet time of walking and meditation. Some meditative thoughts and reflections will be shared and then we will walk the Labyrinth together in silent reflection. Bring your own favorite quotes or meditation words to share.'
          },
          {
            name: 'Phone Camera Photography w/ Mark',
            start: '2022-06-24 9:00',
            end: '2022-06-24 10:30',
            type: 'Activity',
            description: 'Mark will share techniques and tips for how to get the most out of a cell phone camera. A brief presentation will be followed by a short walk on grounds to practice techniques. The instructor will be available outside of this class during WUULF to review techniques and/or provide critiques of photo results.'
          },
          {
            name: 'Hike: TBD',
            start: '2022-06-24 9:00',
            end: '2022-06-24 12:00',
            type: 'Activity',
            description: 'Meet at the Lower Pavilion to join in for a morning hike.'
          },
          {
            name: 'Lunch',
            start: '2022-06-24 12:00',
            end: '2022-06-24 13:00',
            type: 'Meal',
            description: 'Meals are provided at the Dining Hall. Please remember to bring your name tag. Dietary options available.'
          },
          {
            name: 'Lake Swim (parent supervision required)',
            start: '2022-06-24 13:00',
            end: '2022-06-24 16:30',
            type: 'Activity',
            description: 'Swim at Lake Abiquiu. Note that parent supervision is required, and this is an offsite activity.'
          },
          {
            name: 'Craft: Painting w/ Cindy',
            start: '2022-06-24 13:00',
            end: '2022-06-24 14:30',
            type: 'Activity',
            description: 'Learn to use colorful acrylic paints too create a special memory of WUULF! Join Cindy Fesgen to create underpaintings and then stencil or draw a tree, animal, or other natural shapes contrasting with the background. Appropriate for children and adults with no experience painting to those who are experienced artists. $5 fee.'
          },
          {
            name: 'Talk: John Rowe, Positive Psychology',
            start: '2022-06-24 14:30',
            end: '2022-06-24 16:30',
            type: 'Activity',
            description: 'John Rowe will lead a workshop on Positive Psychology exploring what we know about neuropsychology and how we can use it to improve our quality of life.'
          },
          {
            name: 'Happy Hour & Community Time',
            start: '2022-06-24 16:30',
            end: '2022-06-24 17:30',
            type: 'Community',
            description: 'Come visit with friends at the Lower Pavilian to play yard games, enjoy music, and hang out. There will be snacks and drinks (adult beverages & non-alcoholic beverages available).'          },
          {
            name: 'Dinner',
            start: '2022-06-24 17:30',
            end: '2022-06-24 19:00',
            type: 'Meal',
            description: 'Meals are provided at the Dining Hall. Please remember to bring your name tag. Dietary options available.'
          },
          {
            name: 'Dance Night',
            start: '2022-06-24 19:00',
            end: '2022-06-24 21:00',
            type: 'Community',
            description: 'A night of folk dancing, laughter an remembrance.  No experience required! We will have a professional dancer leading us for a night of movement. This annual event is held In memory of Zip (Rich) Lee who attended WUULF many times. Our first gay wedding held at WUULF was when Rich married Matt Disbrow on Chimney Rock. Rich loved to square dance and was a member of First Unitarian Church in Denver.'
          },
          {
            name: 'Music & Sing-a-long',
            start: '2022-06-24 21:00',
            end: '2022-06-24 22:00',
            type: 'Activity',
            description: 'Participants are invited to bring their acoustic instruments: guitars, fiddles, banjos, etc. and of course your singing voice! If you have a copy of "Rise Up Singing" (which is an awesome sing-a-long songbook) please bring it and we\'ll make music in the evening before retiring at 10:00 pm (Ghost Ranch Quiet Time).'          },
          {
            name: 'Ghost Ranch Quiet Hours',
            start: '2022-06-24 22:00',
            end: '2022-06-24 23:00',
            type: 'Ghost Ranch Activity',
            description: 'Ghost ranch hosts other events, groups, and staff on site. Please be respectful of others, and keep evening activities at a low decibel. In addition, WUULFies (under 18) must be in their rooms by the time quiet hours begin.'          },

          {
            name: 'Breakfast',
            start: '2022-06-25 7:30',
            end: '2022-06-25 8:00',
            type: 'Meal',
            description: 'Meals are provided at the Dining Hall. Please remember to bring your name tag. Dietary options available.'
          },
          {
            name: 'Community Gathering',
            start: '2022-06-25 8:15',
            end: '2022-06-25 9:00',
            type: 'Community',
            description: 'While at ghost ranch, the community minister will hold a daily kid friendly service by the big tree which usually includes a short sermon and singing.'
          },
          {
            name: 'Program Day',
            start: '2022-06-25 9:00',
            end: '2022-06-25 16:30',
            type: 'Youth Programming',
            description: ''
          },
          {
            name: 'Lunch',
            start: '2022-06-25 12:00',
            end: '2022-06-25 13:00',
            type: 'Meal',
            description: 'Meals are provided at the Dining Hall. Please remember to bring your name tag. Dietary options available.'
          },
          {
            name: 'Swim',
            start: '2022-06-25 13:00',
            end: '2022-06-25 16:30',
            type: 'Activity',
            description: 'Visit the pool for a cool way to beat the heat after lunch. Note that kids must be with a responsible adult while at the pool.'
          },
          {
            name: 'Talk: Shamshoian, Humaine Issues',
            start: '2022-06-25 14:30',
            end: '2022-06-25 16:30',
            type: 'Activity',
            description: 'Susan and Kimberly will lead a thoughtful discussion on humane issues. There will be an emphasis on how we are all interconnected and can make a positive difference in our world.'
          },
          {
            name: 'Happy Hour & Community Time',
            start: '2022-06-25 16:30',
            end: '2022-06-25 17:30',
            type: 'Community',
            description: 'Come visit with friends at the Lower Pavilian to play yard games, enjoy music, and hang out. There will be snacks and drinks (adult beverages & non-alcoholic beverages available).'
          },
          {
            name: 'Dinner',
            start: '2022-06-25 17:30',
            end: '2022-06-25 19:00',
            type: 'Meal',
            description: 'Meals are provided at the Dining Hall. Please remember to bring your name tag. Dietary options available.'
          },
          {
            name: 'Talent/No Talent Show',
            start: '2022-06-25 19:00',
            end: '2022-06-25 21:00',
            type: 'Community',
            description: 'A WUULF tradition! Do you have an entertaining act to share, solo or as part of a group? No talent is required--after all, this is a “No Talent/Talent” show! The number and duration of acts will be limited in the interest of time.  Plenty of laughter is guaranteed. Drawings for our annual raffle to support the WUULF scholarship fund will take place throughout the evening. Don\'t forget to buy your tickets!'
          },
          {
            name: 'Music & Sing-a-long',
            start: '2022-06-25 21:00',
            end: '2022-06-25 22:00',
            type: 'Activity',
            description: 'Participants are invited to bring their acoustic instruments: guitars, fiddles, banjos, etc. and of course your singing voice! If you have a copy of "Rise Up Singing" (which is an awesome sing-a-long songbook) please bring it and we\'ll make music in the evening before retiring at 10:00 pm (Ghost Ranch Quiet Time).'          },
          {
            name: 'Ghost Ranch Quiet Hours',
            start: '2022-06-25 22:00',
            end: '2022-06-25 23:00',
            type: 'Ghost Ranch Activity',
            description: 'Ghost ranch hosts other events, groups, and staff on site. Please be respectful of others, and keep evening activities at a low decibel. In addition, WUULFies (under 18) must be in their rooms by the time quiet hours begin.'
          },

          {
            name: 'Breakfast',
            start: '2022-06-26 7:30',
            end: '2022-06-26 8:00',
            type: 'Meal',
            description: 'Meals are provided at the Dining Hall. Please remember to bring your name tag. Dietary options available.'
          },
          {
            name: 'Community Gathering Fairwell',
            start: '2022-06-26 8:45',
            end: '2022-06-26 10:00',
            type: 'Community',
            description: 'For our final gathering as a comminity at WUULF, we have a traditional way to say goodbye. We all may "Linger" a little longer.'
          },
        ],
        eventColors: [
          {
            eventType: 'Meal',
            color: 'purple'
          },
          {
            eventType: 'Community',
            color: 'green'
          },
          {
            eventType: 'Activity',
            color: 'orange'
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