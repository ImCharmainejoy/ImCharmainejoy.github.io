<template>
  <v-container
    id="awards"
    class="pa-0">
    <v-card
      id="awards"
      prepend-icon="mdi-trophy-award"
      variant="flat"
      title="Awards & Recognitions">
      <v-row
        align="center"
        class="fill-height"
        justify="center"
      >
        <template v-for="(item, i) in items" :key="i">
          <v-col
            cols="4"
            md="4"
          >
            <v-img
              :src="item.img"
              :width="smAndUp ? '200' : '150'"
              cover
              class="rounded-lg"
              hover
            >
              <div
                :class="isHovering ? 'opacity-100' : 'opacity-0'"
                class="d-flex align-center justify-center transition-opacity duration-500"
                style="height: 100%; background: rgba(0,0,0,0.4); color: white;"
              >
              </div>
            </v-img>
          </v-col>
        </template>
      </v-row>
      <v-card-text class="text-center pa-4">
        <p class="text-h7 font-family font-weight-medium">
            These are some of my notable awards and recognitions I have received for my work and contributions.
        </p>
      </v-card-text>
    </v-card>
</v-container>
</template>
<script setup>
  const { smAndUp } = useDisplay()

  import awards1 from '@/assets/images/awards1.png'
  import awards2 from '@/assets/images/awards2.png'
  import awards3 from '@/assets/images/awards3.png'

  const items = [{
    title: 'School Class & Records Management System',
    text: 'The frontend stack was constructed with Vue v2, JavaScript, ECMAScript, Vuetify v2, and Vuex v3.',
    link: 'https://github.com/ImCharmainejoy/Iamcj.',
    img: awards1
  },
  {
    title: 'Sales Tracker System',
    text: 'The largest free online frontend event. ever.',
    link: 'https://github.com/ImCharmainejoy/Iamcj.',
    img: awards2
  },
  {
    title: 'Vaccination System',
    text: 'The frontend stack was constructed with Vue v2, JavaScript, ECMAScript, Vuetify v2, Nuxt v2, and Vuex v3.',
    link: 'https://github.com/ImCharmainejoy/Iamcj.',
    img: awards3
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
