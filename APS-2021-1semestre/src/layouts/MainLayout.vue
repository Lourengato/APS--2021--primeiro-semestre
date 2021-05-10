<template>
  <q-layout view="lHh Lpr lFf">
     <q-header reveal class="bg-teal">
        <q-toolbar>
          <q-toolbar-title>Informações Corona Vírus</q-toolbar-title>
        </q-toolbar>
      </q-header>
    <q-page-container>
      <q-page-sticky position="top" expand class="bg-teal text-white">
          <q-toolbar>
            <q-btn flat round dense icon="map" />
            <q-toolbar-title>Title</q-toolbar-title>
          </q-toolbar>
        </q-page-sticky>
      <router-view />
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
