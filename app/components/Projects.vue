<template>
  <v-container
    id="projects"
    class="pa-0">
    <v-card
      id="projects"
      prepend-icon="mdi-folder-multiple"
      variant="flat"
      title="Projects">
      <v-row
        align="center"
        class="fill-height"
        justify="center"
      >
        <template v-for="(item, i) in items" :key="i">
          <v-col cols="6" md="6"
            v-if="i % 2 === 0">
            <v-card-title class="text-h6 d-flex flex-column">
              <p class="mt-4">
                {{ item.title }}
              </p>
              <div>
                <p class="ma-0 text-body-1 font-weight-bold">
                  {{ item.text }}
                </p>
                <p class="text-caption font-weight-medium">
                  {{ item.subtext }}
                </p>
              </div>
            </v-card-title>
          </v-col> 
          <v-col
            cols="6"
            md="6"
          >
            <v-hover v-slot="{ isHovering, props }">
            <v-img
              v-bind="props"
              :src="item.img"
              height="300"
              cover
              class="rounded-lg"
            >
              <div
                :class="isHovering ? 'opacity-100' : 'opacity-0'"
                class="d-flex align-center justify-center transition-opacity duration-500"
                style="height: 100%; background: rgba(0,0,0,0.4); color: white;"
              >
                <v-btn variant="outlined" color="white" :href="item.link" target="_blank">View Project</v-btn>
              </div>
            </v-img>
          </v-hover>
          </v-col>
          <v-col cols="6" md="6"
            v-if="i % 2 !== 0">
            <v-card-title class="text-h6 d-flex flex-column break-word">
              <p class="mt-4 break-word">
                {{ item.title }}
              </p>
              <div>
                <span class="ma-0 text-body-1 font-weight-bold break-word">
                  {{ item.text }}
                </span>
              </div>
            </v-card-title>
          </v-col> 
        </template>
      </v-row>
    </v-card>
</v-container>
</template>
<script setup>
  import project1 from '@/assets/images/proj1.png'
  import project2 from '@/assets/images/proj2.png'
  import project3 from '@/assets/images/proj3.png'

  const items = [{
    title: 'School Class & Records Management System',
    text: 'The frontend stack was constructed with Vue v2, JavaScript, ECMAScript, Vuetify v2, and Vuex v3.',
    link: 'https://github.com/ImCharmainejoy/Iamcj.',
    img: project1
  },
  {
    title: 'Sales Tracker System',
    text: 'The largest free online frontend event. ever.',
    link: 'https://github.com/ImCharmainejoy/salesTracker',
    img: project2
  },
  {
    title: 'Vaccination System',
    text: 'The frontend stack was constructed with Vue v2, JavaScript, ECMAScript, Vuetify v2, Nuxt v2, and Vuex v3.',
    link: 'https://github.com/ImCharmainejoy/Iamcj.',
    img: project3
  }]
</script>

<style scoped>
.standalone-img {
  transition: transform 0.4s cubic-bezier(0.4, 0, 0.2, 1), filter 0.4s ease;
  cursor: pointer;
  border-radius: 8px; /* Optional: gives it a clean look */
}

.is-hovered {
  transform: scale(1.05);
  filter: brightness(1.1);
}

.transition-opacity {
  transition: opacity 0.3s ease-in-out;
}
</style>
