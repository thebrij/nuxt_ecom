<template>
  <v-bottom-navigation
    :value="value"
    color="primary"
    v-bind="localAttrs"
    
  >
    <v-btn>
      <span>Wish list</span>

      <v-icon>mdi-heart</v-icon>
    </v-btn>

    <v-btn :to="{ name: 'index'}">
      <span>Home</span>
      <v-icon>mdi-home</v-icon>
    </v-btn>

    <v-btn>
      <span>Account</span>
      <v-icon>mdi-account-circle</v-icon>
    </v-btn>
    <v-btn>
      <span>Cart</span>
      <v-icon>mdi-cart</v-icon>
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