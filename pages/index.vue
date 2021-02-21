<template>
  <v-card
    max-width="400"
    class="mx-auto"
  >
    <v-app-bar
      dark
      color="#1F7087"
    >
      <!-- <v-app-bar-nav-icon></v-app-bar-nav-icon> -->

            <v-toolbar-title v-if="$nuxt.isOffline">You are offline</v-toolbar-title>
            <v-toolbar-title v-if="$nuxt.isOnline">HunarMand</v-toolbar-title>

      <v-spacer></v-spacer>

      <!-- <v-btn class="info" small>
          Become A Member
      </v-btn> -->
    </v-app-bar>

    <v-container>
      <v-row dense>
        

        <v-col
        sm="12"
         height="auto"
          v-for="(item, i) in items"
          :key="i"
          cols="12"
        >
          <v-card
            :color="item.color"
            dark
          >
            <div class="d-flex  justify-space-between">
              <div>

                <v-card-title class="headline" v-text="item.title"></v-card-title>

                <v-card-actions>
                <a 
                target="blank" 
                style="text-decoration:none;" 
                :href="whatsappURL + number">
                   <v-btn small color="#4bec68">
                       Contact Me On<v-icon class="">mdi-whatsapp</v-icon> 
                    </v-btn> 
                </a>
               
                </v-card-actions>
                 <v-card-actions>
               
                 <a 
                target="blank" 
                style="text-decoration:none;" 
                href="https://web.facebook.com/HunarMand-104792168326993/?view_public_for=104792168326993">
                 
                    <v-btn small color="#1877f2">
                       Contact Me On <v-icon class="">mdi-facebook</v-icon> 
                    </v-btn> 
                </a>
                </v-card-actions>
              </div>

              <v-avatar
                class="ma-3"
                size="125"
                tile
              >
                <v-img :src="item.src"></v-img>
              </v-avatar>
            </div>
          </v-card>
        </v-col>
      </v-row>
    </v-container>
  </v-card>
</template>
<script>
  export default {
    layout : 'empty',
    data: () => ({
        whatsappURL : 'https://wa.me/',
        number : '+923201297500',
      items: [
        {
          color: 'purple',
          src: 'https://images.ctfassets.net/r6ek15msiuv1/1ZCq2LZXgm6Xu9TDpNcezW/20b71993b3ed1cdd572ba2a0d24aa058/electrician-requirements-state.jpg',
          title: 'Electrician',
          artist: '',
        },
        {
          color: 'pink',
          src: 'https://cdn.123test.com/content/beroepen/loodgieter.jpg',
          title: 'Plumber',
          artist: '',
        },

        {
          color: 'indigo',
          src: 'https://www.careersinconstruction.ca/sites/default/files/styles/career_banner/public/images/careers/shutterstock_157019144-low.jpg?itok=WINOuZAv',
          title: 'Painter',
          artist: '',
        },
        {
          color: 'blue',
          src: 'https://ix-cdn.b2e5.com/images/19401/19401_fc5111750c714aaca0ea6759365aa31d_1534365375.jpeg',
          title: 'Car Machenic',
          artist: '',
        },
        {
          color: 'grey',
          src: 'https://www.sait.ca/images/Programs%20and%20Courses/Apprenticeships%20and%20Trades/Apprenticeships/motorcycle-mechanic.jpg',
          title: 'Bike Machenic',
          artist: '',
        },
        {
          color: 'cyan',
          src: 'https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcRhkfAF__AcaHiLuJKviRr2QNddUS0T5mjvVA&usqp=CAU',
          title: 'Labour',
          artist: '',
        },
        
      ],
    }),
  }
</script>