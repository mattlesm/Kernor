<template>
  <v-main>
    <v-tabs
      vertical
      centered
      color="#FCA311"
      slider-color="#FCA311"
      slider-size="8"
    >
      <v-tab
        v-for="divinity of pantheon"
        :key="divinity.id"
      >
        {{ divinity.name }}
      </v-tab>

      <v-tab-item
        v-for="divinity of pantheon"
        :key="divinity.id"
        class="ma-5"
      >
        <Divinity :divinityList="divinity"/>
      </v-tab-item>

    </v-tabs>
  </v-main>
</template>

<style scoped>
  .v-tab {
    color: #14213D;
  }
</style>

<script>
  import pantheon_json from  '~/static/pantheon.json'
  import Divinity from '@/components/Divinity.vue'

  export default {
    components: {
      Divinity
    },
    name: 'Pantheon',
    data() {
      return {
        pantheon: pantheon_json
      }
    }
  };
</script>