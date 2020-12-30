<template>
  <v-bottom-navigation
    :value="value"
    v-bind="localAttrs"
    horizontal
    no-gutters 
    
  >
    <v-btn style="width:50%" >
      <span>ADD TO CART</span>
    </v-btn>

    <v-btn style="width:50%"
      color="primary" >
     <span color="white"> BUY NOW</span>
    </v-btn>


  </v-bottom-navigation>
</template>

<script>
  export default {
    data: () => ({ 
        value: 1 ,
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