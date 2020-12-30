<template>
    <div>
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

        <v-container class="mt-5">
            <v-row no-gutters>
                <v-col cols="12" sm="12" md="12" >
                    <p class="title">
                        Savaliya Technology 4+4 With Wire 4 Socket Extension Boards  (White)
                    </p>
                     <v-row align="center" class="mx-0" >
                            <p class="font-weight-black">
                                <v-rating
                                :value="4.5"
                                color="amber"
                                dense
                                half-increments
                                readonly
                                size="14"
                                ></v-rating>
                            </p>
                            <p class="font-weight-medium grey--text ml-4 ">
                                4.5 (413)
                            </p>
                        </v-row>

                        <v-row align="center" class="mx-0" >
                            <p class="font-weight-black title">
                                    $100
                            </p>
                            <p class="font-weight-medium grey--text ml-4 text-decoration-line-through">
                                    $120
                            </p>
                            <p class="font-weight-medium green--text ml-4">
                                31% off
                            </p>
                        </v-row>
                                            
                                    
                </v-col>
            </v-row>
        </v-container>
        <hr>
        <v-container >
            <v-row>
                <v-col cols="12">
                         <p class="title font-weight-bold">
                            Highlights
                         </p>
                         <p class="font-weight-bold">
                                Heading
                            </p>
                         <p class="text-justify">
                             
                            Morbi mattis ullamcorper velit. Donec orci lectus, aliquam ut, faucibus non, euismod id, nulla.
                        </p>
                         <p class="font-weight-bold">
                                Heading
                            </p>
                         <p class="text-justify">
                             
                            Morbi mattis ullamcorper velit. Donec orci lectus, aliquam ut, faucibus non, euismod id, nulla.
                        </p>

                         <p class="title font-weight-bold">
                            Material & color
                         </p>
                         <v-simple-table dense>
                            <template v-slot:default>
                            <tbody>
                                <tr>
                                <td>Material:</td>
                                <td class="font-weight-bold">Wood</td>
                                </tr>
                            </tbody>
                            <tbody>
                                <tr>
                                <td>Color:</td>
                                <td class="font-weight-bold">Navy Blue </td>
                                </tr>
                            </tbody>
                            </template>
                        </v-simple-table>
                         
                </v-col>
            </v-row>
        </v-container> <hr>
        <v-container class="mb-5">
            <v-row>
                <v-col cols="6" sm="6" class="text-left">
                    <p class="font-weight-medium display-2">
                       <span> 4.5  <v-icon class="display-1" color="amber">mdi-star</v-icon></span>
                    </p>
                </v-col>
                <v-col cols="6" sm="6" class="text-left">
                    <p class="font-weight-medium display-1">
                       (413)
                    </p>
                </v-col>
            </v-row>
            <v-row class="mb-5">
                <v-btn
                text
                :ripple="false"
                class="back-wrapper"
                @click="to">
                <icon
                    name="angle-left"
                    fill="#9e9e9e"
                    height="20px"
                    width="20px"
                    class="d-flex" />
                <p class="display-1 grey--text">
                    Back
                </p>
                </v-btn>
                <v-col cols="12" sm="12" md="12" class="text-left">
                    <v-badge
                        bordered
                        color="amber"
                        icon="mdi-star"
                        overlap
                    >
                        <v-btn
                        class="white--text"
                        color="success"
                        depressed
                        >
                        4.5
                        </v-btn>
                    </v-badge>
                </v-col>
            </v-row>
        </v-container>
        <div >
             <ProductFooter/>

        </div>
      
    </div>
</template>
<script>
import ProductFooter from '@/components/ProductFooter';
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
    methods: {
      to() {
        this.$router.go(-1);
        console.log(this.$router.name);
      },
    }
  }
</script>