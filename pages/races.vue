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
        v-for="race of races"
        :key="race.id"
      >
        {{ race.name }}
      </v-tab>

      <v-tab-item
        v-for="race of races"
        :key="race.id"
        class="ma-5"
      >
        <Race :raceList="race"/>
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
  import races_json from  '~/static/races.json'
  import Race from '@/components/Race.vue'

  export default {
    components: {
      Race
    },
    name: 'Races',
    data() {
      return {
        races: races_json
      }
    }
  };
</script>