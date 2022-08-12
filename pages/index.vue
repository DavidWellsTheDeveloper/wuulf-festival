<template>
  <v-container fluid grid-list-xs class="px-0">
    <v-row>
      <v-col>
        <v-parallax src="/1920-1080/19453143_10213404592897539_8945399834199640570_o.jpg" :height="parallaxHeight + 200">
          <h1 class="my-5 text-center" id="welcome">WUULF 2023</h1>
          <h2 class="my-5 text-center">Theme Coming Soon</h2>
          <h3 class="my-5 text-center">June 18th-25th</h3>
        </v-parallax>
      </v-col>
    </v-row>
    <v-row>
      <v-col>
        <v-divider></v-divider>
          <v-alert
            border="top"
            color="primary"
          >
            <h3><i>“There is no power for change greater than a community discovering what it cares about.”</i></h3> <small>-MARGARET J. WHEATLEY</small>
          </v-alert>
      </v-col>
    </v-row>

    <v-divider></v-divider>
    
    <v-row>
      <v-col>
        <v-card class="my-5 elevation-0" color="transparent">
          <v-card-title primary-title>
            The Western Unitarian Universalist Life Festival
          </v-card-title>
          <v-card-subtitle>
            About WUULF
          </v-card-subtitle>
          <v-card-text>
            We are a friendly, intergenerational camp seeking 
            to build a close knit community in which we can 
            live out our UU principles an purposes —a place 
            where participants of all ages can spend time 
            focusing on their own interests, and spend time 
            together. We are a loving community from a 
            diverse set of age groups, backgrounds, and 
            cultures who gather at <b>Ghost Ranch in Abiquiu, 
            New Mexico</b> each year to express our appreciation 
            for each other and our world. We would love to 
            see you there for our relaxing, rejuvenating, and 
            above all, welcoming, week in the New Mexico sun!
          </v-card-text>
        </v-card>
      </v-col>
    </v-row>
    <v-row>
      <v-col cols="12" xl="9" lg="8">
        <AboutWuulf></AboutWuulf>
      </v-col>
      <v-col cols="12" lg="4" xl="3">
        <BoardMembers :members="board"></BoardMembers>
      </v-col>
    </v-row>
    <v-row>
      <v-col cols="12" md="6" align-self="center">
        <Wuulf2023></Wuulf2023>
      </v-col>
      <v-col cols="12" md="6"  align-self="center">
        <v-parallax src="/1920-1080/19243087_10213417605702851_6951291830362793520_o.jpg" :height="parallaxHeight"></v-parallax>
      </v-col>
    </v-row>
    <v-row>
      <v-col cols="12" md="6" align-self="center" :order="$vuetify.breakpoint.smAndDown?'last':'first'">
        <v-parallax src="/1920-1080/19453092_10213417610382968_8204368204190326979_o.jpg" :height="parallaxHeight"></v-parallax>
      </v-col>
      <v-col cols="12" md="6" align-self="center">
        <WuulfTheme></WuulfTheme>
      </v-col>
    </v-row>
    <v-row>
      <v-col cols="12" md="6" align-self="center">
        <Minister></Minister>
      </v-col>
      <v-col cols="12" md="6" align-self="center">
        <v-parallax src="/1920-1080/47a3dd07b3127ccef2e15196d3a100000013100azswldq5znmwpbz4e.jpg" :height="parallaxHeight"></v-parallax>
      </v-col>
    </v-row>
    <v-row>
      <v-col>
        <Calendar></Calendar>
      </v-col>
    </v-row>
    <v-row>
      <v-col>
        <Registration></Registration>
                
        <JotForm></JotForm>
      </v-col>
    </v-row>
  </v-container>
</template>

<script>
import Registration from '~/components/Registration.vue'
export default {
  components: { Registration },
  name: 'IndexPage',
  data() {
    return {
      board: [
        {
          name: "Sarah Weed",
          position: "Director"
        },
        {
          name: "Spencer Hachmeiser",
          position: "Ghost Ranch and Beyond"
        },
        {
          name: "Gary Rieser",
          position: "Treasurer"
        },
        {
          name: "Kiver Woodruff",
          position: "Youth Programming"
        },
        {
          name: "David Wells",
          position: "Communications & Registrar"
        }
      ]
    }
  },
  computed: {
    parallaxHeight() {
       switch (this.$vuetify.breakpoint.name) {
        case 'xs': return 350
        case 'sm': return 400
        case 'md': return 350
        case 'lg': return 500
        case 'xl': return 550
      }
    }
  },
}
</script>

<style lang="scss" scoped>
  
</style>