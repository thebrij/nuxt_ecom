<template>

  <v-app>
    <v-navigation-drawer
      v-model="drawer"
      :mini-variant="miniVariant"
      :clipped="clipped"
      fixed
      app>
    <v-list>
        
        <v-list-item
          v-for="(item, i) in items"
          :key="i"
          :to="item.to"
          router
          exact
        >
          <v-list-item-action>
              <v-icon>{{ item.icon }}</v-icon>
          </v-list-item-action>


          <v-list-item-content>
            <v-list-item-title v-text="item.title" />
          </v-list-item-content>


        </v-list-item>
      </v-list>
    </v-navigation-drawer>

    <v-app-bar :clipped-left="clipped" fixed color="white" app>

      
        <v-app-bar-nav-icon  @click.stop="drawer = !drawer" />

     

     
        <!-- <v-icon @click="back"> mdi-keyboard-backspace</v-icon> -->
     
     
    
      <v-toolbar-title v-text="title" />
      <v-spacer />
        <v-btn
          icon
          @click.stop="rightDrawer = !rightDrawer"
        >
          <v-icon>mdi-menu</v-icon>
        </v-btn>
    </v-app-bar>

    <v-main>
      <div>
        <nuxt />
      </div>
    </v-main>
    <v-navigation-drawer
      v-model="rightDrawer"
      :right="right"
      temporary
      fixed
    >
      <v-list>
        <v-list-item @click.native="right = !right">
          <v-list-item-action>
            <v-icon light>
              mdi-repeat
            </v-icon>
          </v-list-item-action>
          <v-list-item-title>Switch {{route}}(click me)</v-list-item-title>
        </v-list-item>
      </v-list>
    </v-navigation-drawer>
  </v-app>
</template>

<script>

export default {
  
  data () {
    return { 
      clipped: false,
      drawer: false,
      fixed: true, 
      route: 'w',
      links: [
        'Courses',
        'Home',
        'Books',
       
      ],
      items: [
        {
          icon: 'mdi-lock',
          title: 'Welcome',
          to: '/'
        },
        {
          icon: 'mdi-chart-bubble',
          title: 'Inspire',
          to: '/pages/about'
        },
        
      ],
      miniVariant: false,
      right: true,
      rightDrawer: false,
      title: 'Shop'
    }
  },

}
</script>

