<template>
  <q-page padding>
    <!-- QBadge -->
    <div class="q-pa-md q-gutter-sm">
      <q-btn push color="white" text-color="primary" label="Uvećaj" @click="uvecaj()">
      </q-btn>
      <q-btn dense color="white" text-color="primary" label="Resetiraj" class="q-ml-md" @click="resetiraj()">
      </q-btn>
    </div>

    <!-- QCard -->
   <div class="q-pa-md row items-start q-gutter-md">
      <q-card class="my-card">
        <q-card-section>
          {{ brojac }}
        </q-card-section>
      </q-card>
    </div>

    
    <!-- QInput -->
    <div class="q-pa-md row items-start q-gutter-md">
     <q-input v-model="broj1" label="Broj 1"/>
     <q-input v-model="broj2" label="Broj 2"/>
     <q-btn flat @click="zbroji">Zbroji</q-btn>
    </div>
    
    <!-- QCard -->
    <div class="q-pa-md row items-start q-gutter-md">
      <q-card class="my-card">
        <q-card-section>
          {{ broj3 }}
        </q-card-section>
      </q-card>
    </div>

    <div class="q-pa-md row items-start q-gutter-md">
      <q-input v-model="tekst1">Unesi tekst</q-input>
      <q-btn flat @click="spremi">Spremi</q-btn>
    </div>

    <div class="q-pa-md row items-start q-gutter-md">
    <q-card class="my-card text-white" style="background: radial-gradient(circle, #38a2ff 0%, #214a88 100%)">
      <q-card-section v-for="item in tekst" :key="item">
        <div class="Tekst1">{{ item }}</div>
      </q-card-section>

      <q-card-section class="q-pt-none">  
         {{ lorem }}
      </q-card-section>
    </q-card>
    </div>

  </q-page>
</template>

<script setup>
import { ref } from 'vue'

const brojac = ref(0)
const broj1 = ref('')
const broj2 = ref('')
const broj3 = ref(0)

const tekst1 = ref('')
const tekst = ref([])

broj1.value = ''
broj2.value = ''

function spremi() {
  tekst.value.push(tekst1.value)
}

function zbroji() {
  broj3.value = parseInt(broj1.value) + parseInt(broj2.value)
  console.log(broj3.value)
}

function uvecaj() {
  console.log("uvećaj")
  brojac.value ++
}

function resetiraj() {
  console.log("resetiraj")
  brojac.value = 0
}
</script>
