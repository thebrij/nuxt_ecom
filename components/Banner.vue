<template>
  <v-card>
   
    <v-carousel
      :continuous="false"
      :cycle="cycle"
      :show-arrows="false"
      hide-delimiter-background
      delimiter-icon="mdi-minus"
      height="110"
    >


    <v-carousel-item v-for="(image, i) in images" :key="i" >
        <v-img
        lazy-src="https://picsum.photos/id/11/10/6"
        max-height="120"
        :src="image"
        ></v-img>


    </v-carousel-item>

    </v-carousel>
  </v-card>
</template>
<script>
  export default {
    data () {
      return {
        images: [
          'https://images.prismic.io/kasasmart/461fb70e2405322ccd5e0e4fffd82841474484cb_hs200-product-banner.jpg?auto=compress,format',
          'https://m.media-amazon.com/images/S/aplus-media/vc/9af717a6-8e1c-43f5-856c-6983f4a0ada4._CR0,0,970,300_PT0_SX970__.jpg',
         'https://www.justdealindia.com/upload/1537002538modular-switches-banner.jpg',
          'https://www.areena.co.in/images/Electricals/switches/banner.jpg'
        ],
        cycle: true,
      }
    },
  }
</script>