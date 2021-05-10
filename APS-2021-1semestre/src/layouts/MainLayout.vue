<template>
  <q-layout view="lHh Lpr lFf" class="bg-teal-1">
    <q-page-container style="padding-top: 60px">
      <router-view />
      <q-page-sticky position="top" expand class="bg-teal text-white">
        <q-toolbar>
            <q-btn flat round dense icon="medical_services" />
              <q-toolbar-title>Informações Covid-19</q-toolbar-title>
            </q-toolbar>
        </q-page-sticky>
    </q-page-container>
  </q-layout>
</template>

<script>
export default {
  name: 'MainLayout',
  data () {
    return {
      leftDrawerOpen: false
    }
  }
}
</script>
