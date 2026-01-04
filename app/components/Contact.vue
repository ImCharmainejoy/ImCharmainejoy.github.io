<template>
  <v-card 
    id="contact"
    prepend-icon="mdi-email"
    variant="flat"
    title="Contacts">

    <v-list
      v-for="(item, index) in items":key="index">
      <v-list-item prepend-icon="mdi-phone">
        <v-list-item-title>{{ item.contact_no }}</v-list-item-title>
      </v-list-item>

      <v-list-item prepend-icon="mdi-email">
        <v-list-item-title>{{ item.email_address }}</v-list-item-title>
      </v-list-item>
    </v-list>

    <!-- <v-row justify="left" class="mx-3">
      <v-col xs="1" sm="2" md="2" lg="2"
        v-for="(arrList, arrListIndex) in arraylist":key="arrListIndex">
        <v-btn icon :color="arrList.color" :href="arrList.link" target="_blank" rel="noopener noreferrer">
        <v-icon>{{ arrList.icon }}</v-icon>
        <v-img>{{ arrList.icon }}</v-img>
      </v-btn>
      </v-col>
    </v-row> -->
  </v-card>
</template>
<script setup>
  const items = [
    {
      contact_no: '+63 995 1872 924',
      email_address: 'iamcjrosatace@gmail.com'
    }
  ]
  const arraylist = [
  {
    name: 'LinkedIn',
    link: 'https://www.linkedin.com/in/charmaine-joy-rosatace-397808105/',
    icon: 'mdi-linkedin',
    color: 'blue'
  },
  {
    name: 'Viber',
    link: 'https://www.viber.com/',
    icon: 'mdi-viber',
    color: 'blue'
  },
  {
    name: 'Telegram',
    link: 'https://www.telegram.org/',
    icon: 'mdi-telegram',
    color: 'blue'
  }
]
</script>