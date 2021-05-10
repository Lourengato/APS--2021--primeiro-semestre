<template>
  <q-page class="flex flex-center">
    <div class="q-pa-md">
      <q-table
        :data="info"
        :columns="columns"
        row-key="name"
      >
      </q-table>
    </div>
  </q-page>
</template>

<script>
import data from '../../data.json';
export default {
  name: 'PageIndex',

   data () {
    return {
      info: data,
      columns: [
        { name: 'local', align: 'left', label: 'Local', field: 'local', sortable: true },
        { name: 'casos', align: 'left', label: 'Casos', field: 'casos', sortable: true },
        { name: 'novos_casos', align: 'left', label: 'Novos Casos', field: 'novos_casos', sortable: true },
        { name: 'casos_por_milhao', align: 'left', label: 'Casos por Milhão', field: 'casos_por_milhao', sortable: true  },
        { name: 'mortes', align: 'left', label: 'Mortes', field: 'mortes', sortable: true  },
      ],
    }
  },

  methods: {
  }
}
</script>
