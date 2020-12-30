<template>
  <v-card>
   
    <v-carousel
      :continuous="false"
      :cycle="cycle"
      :show-arrows="false"
      hide-delimiter-background
      delimiter-icon="mdi-minus"
      height="150"
    >


    <v-carousel-item v-for="(image, i) in images" :key="i" >
        <v-img
        lazy-src="https://picsum.photos/id/11/10/6"
        max-height="150"
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
          'https://picsum.photos/id/11/500/300',
          'https://picsum.photos/id/12/500/300',
          'https://picsum.photos/id/13/500/300',
          'https://picsum.photos/id/14/500/300',
          'https://picsum.photos/id/15/500/300',
        ],
        cycle: true,
      }
    },
  }
</script>