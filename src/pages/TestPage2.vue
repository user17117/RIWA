<template>
  <q-page padding>
    <!-- content -->
    <q-input color="purple-12" label="Unesi ime"></q-input>
    <q-btn @click="dodajIme">Dodaj</q-btn>
    <p></p>
    <div v-for="item in lista" :key="item">
      <div v-if="item !== 'Ivan'" v-show="true">
        {{ item }}
      </div>
    </div>
    <div class="q-pa-md q-gutter-sm">
      <q-btn push color="white" text-color="primary" label="Add Mails" @click="addMail()">
        <q-badge color="orange" floating v-model="addmsg">{{ addmsg }}</q-badge>
      </q-btn>

      <q-btn dense color="purple" round icon="email" class="q-ml-md" @click="delMail()">
        <q-badge color="red" floating v-model="delmsg">{{ delmsg }}</q-badge>
      </q-btn>
    </div>
  </q-page>
</template>

<script setup>
//
import { ref } from 'vue'

const input = ref('')
const lista = ['Ivan', 'Marko', 'Ana', 'David', 'Sara', 'Lara', 'Luka']
const addmsg = ref(21)
const delmsg = ref(4)

input.value = "";

function dodajIme() {
  lista.push(input.value)
  console.log(input.value)
  console.log(lista)
}

function addMail(){
  addmsg.value += 1;
  console.log
}

function delMail(){
  delmsg.value -= 1;
}
</script>
