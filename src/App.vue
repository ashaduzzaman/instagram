<template>
  <v-app>
    <v-app-bar
      flat
      app
      color="white"
      clipped
    >
      <div class="d-flex align-center">
        <v-card outlined width="200" class="pa-2">
          <v-layout>
            <v-flex>
              <v-icon color="grey">mdi-magnify</v-icon>
              <span class="ml-2 grey--text">Search</span>
            </v-flex>
            <v-flex class="text-right">
              <v-icon color="grey">mdi-microphone-outline</v-icon>
            </v-flex>
          </v-layout>
        </v-card>
      </div>

      <v-spacer></v-spacer>
      <v-btn dark elevation="10" color="red" class="text-none mr-5">
        <span><v-icon class="mr-2">mdi-plus</v-icon>Create New Post</span>
      </v-btn>
      <v-btn icon class="mr-5"><v-icon>mdi-email-outline</v-icon></v-btn>
      <v-btn icon class="mr-5"><v-icon>mdi-heart-outline</v-icon></v-btn>
      <v-avatar size="30">
      <img
        src="https://cdn.vuetifyjs.com/images/john.jpg"
        alt="John"
      >
    </v-avatar>
    </v-app-bar>
    <v-navigation-drawer v-model="drawer" permanent app>
      <v-layout class="pa-4">
        <div>Instagram</div>
      </v-layout>
      <v-layout class="mt-10">
        <v-flex>
          <v-layout>
            <v-flex text-center>
              <v-avatar size="70" color="grey">AZ</v-avatar>
              <div class="mt-4 title">Md. Ashaduzzaman</div>
              <div class="mt-1 subtitle-2 grey--text">Dhaka, Bangladesh</div>
              <div class="mt-5">
                <v-layout>
                  <v-flex>
                    <div class="subtitle-2">Post</div>
                    <div class="subtitle-2 grey--text">520</div>
                  </v-flex>
                  <v-flex>
                    <div class="subtitle-2">Followers</div>
                    <div class="subtitle-2 grey--text">5.2 M</div>
                  </v-flex>
                  <v-flex>
                    <div class="subtitle-2">Following</div>
                    <div class="subtitle-2 grey--text">52</div>
                  </v-flex>
                </v-layout>
              </div>
            </v-flex>
          </v-layout>
        </v-flex>
      </v-layout>
      <v-list
        nav
        dense
        class="mt-10"
      >
        <v-list-item-group
          v-model="group"
          active-class="red--text text--accent-4"
        >
          <v-list-item>
            <v-list-item-icon>
              <v-icon>mdi-home-outline</v-icon>
            </v-list-item-icon>
            <v-list-item-title>Feed</v-list-item-title>
          </v-list-item>
          <v-list-item>
            <v-list-item-icon>
              <v-icon>mdi-compass-outline</v-icon>
            </v-list-item-icon>
            <v-list-item-title>Explore</v-list-item-title>
          </v-list-item>
          <v-list-item>
            <v-list-item-icon>
              <v-icon>mdi-pound</v-icon>
            </v-list-item-icon>
            <v-list-item-title>Trending</v-list-item-title>
          </v-list-item>
          <v-list-item>
            <v-list-item-icon>
              <v-icon>mdi-check-decagram</v-icon>
            </v-list-item-icon>
            <v-list-item-title>Top Post</v-list-item-title>
          </v-list-item>
          <v-list-item>
            <v-list-item-icon>
              <v-icon>mdi-account-outline</v-icon>
            </v-list-item-icon>
            <v-list-item-title>People</v-list-item-title>
          </v-list-item>
          <v-list-item>
            <v-list-item-icon>
              <v-icon>mdi-bell-outline</v-icon>
            </v-list-item-icon>
            <v-list-item-title>Notification</v-list-item-title>
          </v-list-item>
          <v-list-item>
            <v-list-item-icon>
              <v-icon>mdi-send-outline</v-icon>
            </v-list-item-icon>
            <v-list-item-title>Direct</v-list-item-title>
          </v-list-item>
          <v-list-item>
            <v-list-item-icon>
              <v-icon>mdi-chart-pie</v-icon>
            </v-list-item-icon>
            <v-list-item-title>Status</v-list-item-title>
          </v-list-item>
          <v-list-item>
            <v-list-item-icon>
              <v-icon>mdi-cog-outline</v-icon>
            </v-list-item-icon>
            <v-list-item-title>Settingst</v-list-item-title>
          </v-list-item>
        </v-list-item-group>
      </v-list>
    </v-navigation-drawer>
    <v-main>
      <ProfilePage/>
    </v-main>
  </v-app>
</template>

<script>
// import HelloWorld from './components/HelloWorld';
import ProfilePage from './pages/ProfilePage'

export default {
  name: 'App',

  components: {
    ProfilePage,
  },

  data: () => ({
    drawer: false,
      group: null,
  }),
  watch: {
      group () {
        this.drawer = false
      },
    },
};
</script>
