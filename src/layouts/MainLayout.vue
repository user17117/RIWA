<template>
  <q-layout view="lHh Lpr lFf">
    <q-header elevated>
      <q-toolbar>
        <q-btn flat dense round icon="menu" aria-label="Menu" @click="toggleLeftDrawer" />

        <q-toolbar-title class="text-h4 text-weight-bold text-center"> Knjižnica Rijeka </q-toolbar-title>

        <div>Quasar v{{ $q.version }}</div>
      </q-toolbar>
    </q-header>

    <q-drawer v-model="leftDrawerOpen" show-if-above bordered>
      <q-list>
        <q-item-label header> Essential Links </q-item-label>

        <EssentialLink v-for="link in linksList" :key="link.label" v-bind="link" />
      </q-list>
    </q-drawer>

    <q-page-container>
      <router-view />
    </q-page-container>
  </q-layout>
</template>

<script setup>
import { ref } from 'vue'
import EssentialLink from '@/components/EssentialLink.vue'

const linksList = [
  {
    label: 'Main Page',
    caption: 'Go to main page',
    icon: 'home',
    link: '/',
  },
  {
    label: 'Popis Knjiga',
    caption: 'Prikaži popis knjiga',
    icon: 'library_books',
    link: '/popis_knjiga/',
  },
  {
    label: 'Pretraživanje',
    caption: 'Pretraži knjižnicu',
    icon: 'search',
    link: '/pretrazivanje/',
  },
  {
  label: 'O nama',
  icon: 'info',
  link: '/o_nama/',
  },
  {
  label: 'Lokacija',
  caption: 'Naša lokacija',
  icon: 'location_on',
  link: '/lokacija/',
  },
  {
  label: 'Log In',
  caption: 'Prijava',
  icon: 'login',
  link: '/login/',
  },
  {
  label: 'Registracija',
  caption: 'Registriraj se',
    icon: 'person',
    link: '/registracija/',
  },
]

const leftDrawerOpen = ref(false )

function toggleLeftDrawer() {
  leftDrawerOpen.value = !leftDrawerOpen.value
}
</script>
