<template>
    <v-navigation-drawer
      app 
      permanent
      left
      color=#14213D
      dark
    >
      <h1>Kernor</h1>

      <v-list>
        <v-list-item
          v-for="item in items"
          :key="item.title"
          :to="item.route"
          color="#FCA311"
        >
          <v-list-item-icon>
            <v-icon right left> {{ item.icon }}</v-icon>
          </v-list-item-icon> 

          <v-list-item-content>
            <v-list-item-title>{{ item.title }}</v-list-item-title>
          </v-list-item-content>

        </v-list-item>
      </v-list>
    </v-navigation-drawer>
</template>

<style>
  h1 {
    color: #FFFFFF;
    margin-left:12%;
    margin-top:15%;
    margin-bottom:15%;
    font-family: 'Cinzel Decorative', cursive;
    font-size: 45px;
  }
</style>

<script>

  export default {
    name: 'Menu',
    data() {
      return {
        items: [
          { title: 'PANTHÉON', icon: 'mdi-atom-variant', route:'/pantheon' },
          { title: 'HISTOIRE', icon: 'mdi-book-open-page-variant-outline', route: '/races' },
          { title: 'MAPS', icon: 'mdi-map-legend', route: '/maps' },
        ]
      }
    }
  };
</script>