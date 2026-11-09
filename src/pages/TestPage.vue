<template>
  <q-page padding>
    <!-- content -->
     <p v-html = "msg_html"></p>
     {{ msg_html }}
     {{ msg }}
     <p v-text="msg"></p>
     <p v-for="item in days" :key="item">
      <button v-if="item=='Ponedjeljak'">
        {{ item }} *
      </button>
      <button v-else v-show="false">
        {{ item }}
      </button>
     </p>
     <a :href="link.url" :target="link.target"> {{ link.text }}</a>
     <q-input color="purple-12" v-model="text" label="Unesi ime"></q-input>

  </q-page>
</template>

<script setup>
//
import {ref} from 'vue'

const msg = "Pozdrav";                   
const msg_html = "<h1>Naslov</h1>";
const days = ['Ponedjeljak', 'Utorak', 'Srijeda', 'Četvrtak', 'Petak', 'Subota', 'Nedjelja'];
const link = {
  url: 'http://www.google.com',
  target: '_blank',
  text: 'Google'
}
const text = ref('')
text.value = "text"
</script>
