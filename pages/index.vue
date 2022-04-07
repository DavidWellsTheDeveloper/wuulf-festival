<template>
  <v-container fluid grid-list-xs class="px-0">
    <v-row justify="center" align="center">
      <v-col cols="12" sm="8" md="6">
        <h1 class="my-5 text-center" id="welcome">Welcome To WUULF</h1>
      </v-col>
    </v-row>
    <v-row>
      <v-col>
        <v-parallax src="/1920-1080/19453143_10213404592897539_8945399834199640570_o.jpg" :height="parallaxHeight"></v-parallax>
      </v-col>
    </v-row>
    <v-row>
      <v-col>
        <v-divider></v-divider>
          <v-alert
            border="top"
            color="green darken-3"
          >
            <h3><i>“There is no power for change greater than a community discovering what it cares about.”</i></h3> <small>-MARGARET J. WHEATLEY</small>
          </v-alert>
        <v-divider></v-divider>
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
      <v-col cols="12" md="6" align-self="center">
        <Wuulf2022></Wuulf2022>
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
        <v-parallax src="/1920-1080/47a3dd07b3127ccef2e15196d3a100000013100azswldq5znmwpbz4e.jpg"></v-parallax>
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
  computed: {
    parallaxHeight() {
       switch (this.$vuetify.breakpoint.name) {
        case 'xs': return '350'
        case 'sm': return '400'
        case 'md': return '350'
        case 'lg': return '400'
        case 'xl': return '450'
      }
    }
  },
}
</script>

<style lang="scss" scoped>
  
</style>