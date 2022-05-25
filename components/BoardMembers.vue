<template>
    <v-container grid-list-xs>
        <v-card color="primary">
          <v-card-title>WUULF 2022 Board Members</v-card-title>
          <v-card-text>
            <v-list>
              <v-list-item v-for="member in members" :key="member.name">
                <v-list-item-content>
                  <v-list-item-title>{{ member.name }}</v-list-item-title>
                  <v-list-item-subtitle>{{ member.position }}</v-list-item-subtitle>
                </v-list-item-content>
              </v-list-item>
            </v-list>
          </v-card-text>
        </v-card>
    </v-container>
</template>

<script>
    export default {
        props: {
            members: {
                type: Array,
                required: true
            },
        },
    }
</script>

<style lang="scss" scoped>

</style>