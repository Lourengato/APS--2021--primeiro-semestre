<template>
  <q-page>
    <div class="q-pa-md">
      <q-img
      src="../assets/header.jpg"
      spinner-color="white"
      height="200px"
      class="q-mb-sm"
    />
      <q-table
        :data="info"
        :columns="columns"
        :dense="$q.screen.lt.md"
        row-key="name"
        table-header-class="text-teal"
        :filter="filter"
        hide-bottom
        :pagination="{rowsPerPage: 0}"
      >
        <template v-slot:top>
          <div class="fit justify-center">
            <q-input borderless dense debounce="300" outlined  v-model="filter" placeholder="Pesquisar">
              <template v-slot:append>
                <q-icon name="search" />
              </template>
            </q-input>
          </div>
        </template>
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
      filter: '',
      info: data,
      columns: [
        { name: 'local', align: 'left', label: 'Local', field: 'local', sortable: true, headerClasses: 'bg-grey-2', classes: 'bg-grey-2 ellipsis', },
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
