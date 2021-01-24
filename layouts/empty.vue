<template>
  <v-app dark>


    <v-main>

       <v-row>
      <v-col class="text-center">
      <v-toolbar
      :color="'success'"
      dark
    >
    HunarMand
    <v-spacer></v-spacer>
   <a target="blank" style="text-decoration:none;" class="white--text" :href="whatsappURL"><v-btn  small class="success">
     Become A Member </v-btn>
  </a>
   

    </v-toolbar>
 
      </v-col>
    </v-row>

      <v-container>
        <nuxt />
      </v-container>

    </v-main>

  </v-app>
</template>

<script>
export default {
  data () {
    return {
      whatsappURL : 'https://wa.me/+923108559858',
      clipped: false,
      drawer: false,
      fixed: false,
      items: [
        {
          icon: 'mdi-apps',
          title: 'Welcome',
          to: '/'
        },
        {
          icon: 'mdi-chart-bubble',
          title: 'Inspire',
          to: '/inspire'
        }
      ],
      miniVariant: false,
      right: true,
      rightDrawer: false,
      title: 'Vuetify.js'
    }
  },
  methods: {
    

  }
}
</script>
