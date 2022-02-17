<template>
  <v-container fluid grid-list-xs>
    <v-row justify="center" align="center">
      <v-col cols="12" sm="8" md="6">
        <h1 class="my-5 text-center" id="welcome">Welcome To WUULF</h1>
      </v-col>
    </v-row>
    <v-row>
      <v-col>
        <v-parallax src="/1920-1080/47a3dd07b3127ccef2e15196d3a100000013100azswldq5znmwpbz4e.jpg"></v-parallax>
      </v-col>
    </v-row>
    <v-row>
      <v-col>
        <v-divider></v-divider>
        <v-card class="my-5">
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
      <v-col>
        <Calendar></Calendar>
        Lorem ipsum, dolor sit amet consectetur adipisicing elit. Excepturi veniam sapiente tempore minus eveniet quasi nostrum ratione? Distinctio atque rerum esse tenetur, maiores deserunt dolorem, sunt explicabo, mollitia velit fugiat? Lorem ipsum dolor sit amet consectetur, adipisicing elit. Quia optio nesciunt ipsa sed aliquid voluptatibus obcaecati temporibus excepturi corrupti debitis, quae impedit rerum iusto laboriosam, pariatur dolorum, iure nobis dolorem. Lorem ipsum, dolor sit amet consectetur adipisicing elit. Aperiam ex accusamus rerum amet voluptatem, esse, fugiat, voluptas magni recusandae dicta neque blanditiis alias! Amet quae sint ex dolore facere magnam? Lorem ipsum dolor sit, amet consectetur adipisicing elit. Neque recusandae rerum iure voluptates error natus in doloribus, odio impedit molestias laudantium praesentium pariatur laborum eligendi perspiciatis dicta facilis doloremque debitis. Lorem ipsum dolor sit amet consectetur adipisicing elit. Repudiandae, aliquid! Officia cumque assumenda, vel deserunt quam velit! Nisi laudantium error explicabo, omnis voluptate nihil distinctio, animi totam dignissimos quasi voluptates. Lorem ipsum, dolor sit amet consectetur adipisicing elit. Accusantium tempora cumque animi eos iure totam in deleniti mollitia voluptates voluptas maxime quos ipsam corrupti, ipsum architecto. Mollitia deserunt ea illo?
      </v-col>
    </v-row>
    <v-row>
      <v-col>
        <Registration></Registration>
                Lorem ipsum, dolor sit amet consectetur adipisicing elit. Excepturi veniam sapiente tempore minus eveniet quasi nostrum ratione? Distinctio atque rerum esse tenetur, maiores deserunt dolorem, sunt explicabo, mollitia velit fugiat? Lorem ipsum dolor sit amet consectetur, adipisicing elit. Quia optio nesciunt ipsa sed aliquid voluptatibus obcaecati temporibus excepturi corrupti debitis, quae impedit rerum iusto laboriosam, pariatur dolorum, iure nobis dolorem. Lorem ipsum, dolor sit amet consectetur adipisicing elit. Aperiam ex accusamus rerum amet voluptatem, esse, fugiat, voluptas magni recusandae dicta neque blanditiis alias! Amet quae sint ex dolore facere magnam? Lorem ipsum dolor sit, amet consectetur adipisicing elit. Neque recusandae rerum iure voluptates error natus in doloribus, odio impedit molestias laudantium praesentium pariatur laborum eligendi perspiciatis dicta facilis doloremque debitis. Lorem ipsum dolor sit amet consectetur adipisicing elit. Repudiandae, aliquid! Officia cumque assumenda, vel deserunt quam velit! Nisi laudantium error explicabo, omnis voluptate nihil distinctio, animi totam dignissimos quasi voluptates. Lorem ipsum, dolor sit amet consectetur adipisicing elit. Accusantium tempora cumque animi eos iure totam in deleniti mollitia voluptates voluptas maxime quos ipsam corrupti, ipsum architecto. Mollitia deserunt ea illo?

      </v-col>
    </v-row>
  </v-container>
</template>

<script>
import Registration from '~/components/Registration.vue'
export default {
  components: { Registration },
  name: 'IndexPage'
}
</script>

<style lang="scss" scoped>
  
</style>