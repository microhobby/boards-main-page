<template>
  <q-layout view="lHh Lpr lFf">
    <q-header elevated>
      <q-toolbar>
        <q-btn
          flat
          dense
          round
          @click="leftDrawerOpen = !leftDrawerOpen"
          icon="menu"
          aria-label="Menu"
        />

        <q-toolbar-title>
          Boards Explorer Project
        </q-toolbar-title>

        <div>Boards v{{ boardsVersion }}</div>
      </q-toolbar>
    </q-header>

    <q-drawer
      v-model="leftDrawerOpen"
      bordered
      content-class="bg-grey-1"
    >
      <q-list>
        <q-item-label header class="text-grey-8">Boards List</q-item-label>
        <EssentialLink
          v-for="link in essentialLinks"
          :key="link.title"
          v-bind="link"
        />
      </q-list>
    </q-drawer>

    <q-page-container>
      <router-view />
    </q-page-container>
  </q-layout>
</template>

<script>
import EssentialLink from 'components/EssentialLink'

export default {
  name: 'MainLayout',

  components: {
    EssentialLink
  },

  data () {
    return {
      boardsVersion: '0.0',
      leftDrawerOpen: false,
      essentialLinks: [
        {
          title: 'Orange Pi Zero',
          caption: 'Open-source single-board computer 48 mm × 46mm',
          icon: 'developer_board',
          link: 'https://quasar.dev'
        },
        {
          title: 'Roduino',
          caption: 'Homemade Arduino by Rodrigo Costa',
          icon: 'developer_board',
          link: 'https://github.com/quasarframework'
        }
      ]
    }
  },
  created () {
    console.log('Created')
  }
}
</script>
