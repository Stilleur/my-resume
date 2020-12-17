<template>
  <v-container>
    <v-row no-gutters>
      <v-col cols="9">
        <v-row no-gutters>
          <v-col>
          {{ fullname }}
          </v-col>
        </v-row>
        <v-row no-gutters>
          <v-col>
            {{ jobTitle }}
          </v-col>
        </v-row>
        <v-row class="details" align="center" no-gutters>
          <v-col v-for="detail in details" :key="detail.text" cols="4" class="my-2">
            <v-icon small color="primary">{{detail.icon}}</v-icon>
            {{detail.text}}
          </v-col>
        </v-row>
      </v-col>
      <v-col align-self="center">
        <v-row justify="center" no-gutters>
          <v-col cols="auto">
            <v-avatar size="120">
              <img :src="picture" :alt="fullname">
            </v-avatar>
          </v-col>
        </v-row>
      </v-col>
    </v-row>
  </v-container>
</template>

<script>
import picture from '../assets/picture.jpg'

export default {
  name: 'Profile',

  data: () => ({
    firstname: 'Cédric',
    lastname: 'Mourgeon',
    jobTitle: 'Front-end Software Engineer',
    picture,
    details: [
      { text: '+41 76 220 81 55', icon: 'mdi-phone' },
      { text: 'cedricmourgeon@gmail.com', icon: 'mdi-email' },
      { text: 'stackoverflow.com/u/2474214', icon: 'mdi-link' },
      { text: 'Avenue du Mont-Blanc 20, 1196 Gland', icon: 'mdi-map-marker' },
      { text: 'Nationalité française', icon: 'mdi-book' },
      { text: '27 ans', icon: 'mdi-account' }
    ]
  }),

  computed: {
    fullname () { return `${this.firstname} ${this.lastname}` }
  }
}
</script>

<style scoped>
.details {
  font-size: 0.7rem;
}
</style>
