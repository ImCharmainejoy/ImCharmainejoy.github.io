<template>
  <v-card
    id="about"
    variant="flat"
  >
  <v-row class="negative-top" align="center">
    <v-col cols="12" sm="12" class="text-center">
      <span class="font-style" :class="smAndUp ? 'text-h4' : 'text-caption'">
        Hi! This is Charmaine Joy Rosatace.
      </span>
    </v-col>
    <v-col cols="12" sm="4" class="text-center"> 
      <v-avatar :size="smAndUp ? '180' : '100'">
        <v-img :src="myAvatar" alt="Iamcj. Avatar"></v-img>
      </v-avatar>
    </v-col>
    <v-col cols="12" sm="8"> 
      <span class="text-caption font-style mb-2">
        An enthusiastic and committed person with a <strong>computer science</strong> background.<br/>
      </span>
      <span class="text-caption font-style pb-5">
        A <strong>frontend web developer</strong> experienced with <strong>Vue</strong> v2, <strong>Javascript</strong>,
        and <strong>Nuxt</strong> v2 and new to Vue v3, Typescript, Nuxt v3, Vite and Pinia. <br/>
      </span>
      <span class="text-caption font-style mb-2">
        A <strong>Proud Filipina</strong> and a dreamer, whose vision is to grow professionally from the ground up 
        and be a better version of myself, all for the glory of God.<br/>
      </span>
      <span class="text-caption font-style">
        I speak fluent Tagalog and English and know basic Japanese.
      </span>
    </v-col>
  </v-row>
  </v-card>
</template>
<script setup>
  import myAvatar from '@/assets/images/me.png'
  const { smAndUp } = 'useDisplay'
</script>
<style scoped>
.negative-top {
  margin-top: -10px
}
</style>
