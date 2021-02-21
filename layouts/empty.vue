<template>
<v-app>
  <v-app-bar
      dark
      fixed
      color="purple"
      
    >
      <!-- <v-app-bar-nav-icon></v-app-bar-nav-icon> -->

            <v-toolbar-title v-if="$nuxt.isOffline">You are offline</v-toolbar-title>
            <v-toolbar-title v-if="$nuxt.isOnline">HunarMand</v-toolbar-title>

      <v-spacer></v-spacer>

      <!-- <v-btn class="info" small>
          Become A Member
      </v-btn> -->
    </v-app-bar>
    
    <v-main>
    <v-container>
    <nuxt />
    </v-container>
    </v-main>
</v-app>
</template>