<template>
  <v-container>
    <v-card>
      <v-row no-gutters>
        <v-col>
          <Profile />
        </v-col>
      </v-row>
      <!-- <v-row>
        <v-col cols="7">
          First Col
        </v-col>
        <v-col>
          Second Col
        </v-col>
      </v-row> -->
    </v-card>
  </v-container>
</template>

<script>
import Profile from './Profile'

export default {
  name: 'Resume',

  components: {
    Profile
  },

  data: () => ({
    //
  })
}
</script>
