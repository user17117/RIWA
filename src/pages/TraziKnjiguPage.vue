<template>
  <q-page padding>
        <q-toolbar-title class="text-h4 text-weight-bold text-left"> Traži knjigu </q-toolbar-title>
        <div class="q-pa-md">
          
    <div class="q-gutter-md" style="max-width: 300px">
    <q-input outlined v-model="text" label="Pretraži knjižnicu" />
    <div class="q-pa-md">
    <q-checkbox v-model="val" label="Pretraživanje po autoru"/>
    <q-checkbox v-model="nal" label="Pretraživanje po naslovu"/>

    <div class="q-pa-md q-gutter-sm">
            <q-btn color="primary" label="Traži" />
          </div>
    
</div>
  </div>
</div>
  </q-page>
</template>

<script setup>
//Search bar
import { ref } from 'vue'
const text = ref('')
const val = ref(false)
const nal = ref(false)

</script>
