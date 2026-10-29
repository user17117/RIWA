<template>
  <q-page padding>
        <q-toolbar-title class="text-h4 text-weight-bold text-left"> Log In </q-toolbar-title>
        <div class="q-pa-md">
        <div class="q-gutter-md" style="max-width: 300px">
          <q-input filled  v-model="korime" label="Korisničko ime" />
          <q-input filled  v-model="lozinka" type="password" label="Lozinka" />


        <div class="q-pa-md q-gutter-sm">
        <q-btn color="primary" label="Potvrdi" />
        </div>

        </div>
        </div>



  </q-page>
</template>

<script setup>
import { ref } from 'vue'

const korime = ref('')
const lozinka = ref('')
</script>