<template>
  <q-page padding>
        <q-toolbar-title class="text-h4 text-weight-bold text-left"> Registracija </q-toolbar-title>

  <div class="q-pa-md">
  <div class="q-gutter-md" style="max-width: 300px">
    <q-input filled  v-model="ime" label="Ime" />
    <q-input filled  v-model="prezime" label="Prezime" />
    <q-input filled  v-model="brtel" label="Broj telefona" />
    <q-input filled  v-model="korime" label="Korisničko ime" />
    <q-input filled  v-model="lozinka" type="password" label="Lozinka" />
    <q-input filled  v-model="mail" label="Email" />

    <div class="q-pa-md q-gutter-sm">
    <q-btn color="primary" label="Potvrdi" />
    </div>

  </div>
</div>

  </q-page>
</template>

<script setup>
import { ref } from 'vue'

const ime = ref('')
const prezime = ref('')
const brtel = ref('')
const korime = ref('')
const lozinka = ref('')
const mail = ref('')
</script>
