<template>
  <v-card
    id="skill"
    variant="flat"
    class="px-2">
    <v-row wrap>
      <v-col xs="12" sm="12" md="4"
       v-for="(item, index) in data.items" :key="index" >
        <v-chip tonal class="text-h5 font-style my-4 mx-5 card-bg-color">
          {{ item.label }}
        </v-chip>
        <v-card-text class="font-style mb-4">
          <div class="mb-4">
            <div class="text-subtitle-1 font-style mb-3">{{ item.description }}</div>
            <div class="text-caption text--secondary font-style">{{ item.subdescription }}</div>
          </div>
        </v-card-text> 
      </v-col>
    </v-row>
  </v-card>
</template>

<script setup lang="ts">
import { ref } from 'vue';
import { useDisplay } from 'vuetify'

const { smAndUp } = useDisplay()

// HTML, CSS, and JavaScript Skillset Overview
const data = ref({
  labels: ['CSS Grid & Flexbox', 'HTML5 & Semantic Markup', 'JavaScript', 'Ecmascript', 'Typescript'],
  items: [
    {
      label: '6+',
      description: 'Years of experience in frontend web development',
      subdescription: 'Over six years of hands-on experience.',
    },{
      label: '7+',
      description: 'Major projects completed',
      subdescription: 'Successfully completed ten significant projects on time and within budget.',
    },{
      label: '9+',
      description: 'Skills acquired through various projects',
      subdescription: 'Acquired more than nine skills to enhance my expertise.',
    }
  ]
});
</script>

<style scoped>
.xs-container {
  box-shadow: 0 0 10px rgba(0,0,0,0.1);
  border-radius: 8px;
  height: 350px; /* Give the chart container a fixed height or min-height */
}
.sm-and-up-container {
  max-width: 800px;
  margin: 20px auto;
  padding: 20px;
  box-shadow: 0 0 10px rgba(0,0,0,0.1);
  border-radius: 8px;
  height: 350px; /* Give the chart container a fixed height or min-height */
}
</style>