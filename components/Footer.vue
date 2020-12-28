<template>
  
    <v-footer
      v-bind="localAttrs"
      padless=true
    >
      <v-card
        flat
        tile
        width="100%"
        class="red text-center"
      >
        <v-card-text>
          <v-btn
            v-for="icon in icons"
            :key="icon"
            class="mx-4"
            icon
            
          >
            <v-icon size="24px" class="">
              {{ icon }}
            </v-icon>
          </v-btn>
        </v-card-text>

       
      </v-card>
    </v-footer>

</template>


<script>
  export default {
    data: () => ({
      icons: [
        'mdi-home',
        'mdi-email',
        'mdi-calendar',
        'mdi-delete',
      ],
      items: [
        'default',
        'absolute',
        'fixed',
      ],
      variant: 'fixed',
    }),
    computed: {
      localAttrs () {
        const attrs = {}

        if (this.variant === 'default') {
          attrs.absolute = false
          attrs.fixed = false
        } else {
          attrs[this.variant] = true
        }
        return attrs
      },
    },
  }
</script>