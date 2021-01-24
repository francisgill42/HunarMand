<template>

  <v-row class="mt-5">
    <v-col sm="12" v-for="(bd,i) in btnData" :key="i" cols="12" class="text-center">
       
         <a target="blank" style="text-decoration:none;" class="white--text" :href="whatsappURL + number">
             <v-btn width="50%" x-large color="success accent-4" class="success"> {{bd.text}} </v-btn>
         </a>
    </v-col>
  </v-row>
</template>

<script>


export default {
layout : 'empty',
data : () => ({
    whatsappURL : 'https://wa.me/',
    number : '+923108559858',
    btnData : [
        {'text' : 'Electrician'},
        {'text' : 'Plumber'},
        {'text' : 'Painter'},
        {'text' : 'Mechanic'},
        {'text' : 'Labour'},
    ] 
})    
}
</script>
