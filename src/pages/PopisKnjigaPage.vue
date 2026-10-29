<template>
  <q-page padding>   
    <!-- content -->
    <q-toolbar-title class="text-h4 text-weight-bold text-left"> Popis knjiga </q-toolbar-title>
    <div class="q-pa-md">
    <q-table
      flat
      bordered
      title="Treats"
      dense
      :rows="rows"
      :columns="columns"
      row-key="name"
    />
</div>
  </q-page>
</template>

<script setup>
//
const columns = [
  {
    name: 'id',
    align: 'left',
    label: 'id',
    field: 'id',
    sortable: true,
    style: {
      fontSize: '14px'
    },
    headerStyle: {
      fontSize: '16px'
    }
  },
  {
    name: 'naslov',
    align: 'left',
    label: 'naslov',
    field: 'naslov',
    sortable: true,
    style: {
      fontSize: '14px'
    },
    headerStyle: {
      fontSize: '16px'
    }
  },
  { name: 'autor', align: 'left', label: 'autor', field: 'autor', sortable: true,
    style: {
      fontSize: '14px'
    },
    headerStyle: {
      fontSize: '16px'
    }},
  { name: 'opis', align: 'left', label: 'opis', field: 'opis', sortable: true,
    style: {
      fontSize: '14px'
    },
    headerStyle: {
      fontSize: '16px'
    }},
  { name: 'slika', align: 'left', label: 'slika', field: 'slika', sortable: true,
    style: {
      fontSize: '14px'
    },
    headerStyle: {
      fontSize: '16px'
    }},
  {
    name: 'stanje',
    label: 'stanje',
    align: 'left',
    field: 'stanje',
    sortable: true,
    style: {
      fontSize: '14px'
    },
    headerStyle: {
      fontSize: '16px'
    },
    sort: (a, b) => Number.parseInt(a, 10) - Number.parseInt(b, 10)
  },
  {
    name: 'status',
    label: 'status',
    align: 'left',  
    field: 'status',
    sortable: true,
    style: {
      fontSize: '14px'
    },
    headerStyle: {
      fontSize: '16px'
    },
    sort: (a, b) => Number.parseInt(a, 10) - Number.parseInt(b, 10)
  }
]

const rows = [
  {
    id:1,
    naslov:'The Very Hungry Caterpillar',
    autor:'Eric Carle',
    opis:'As an added bonus, it includes read-aloud audio of...',
    slika:'',
    stanje:3,
    status:'zauzeta',
  },
]
</script>
