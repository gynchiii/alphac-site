<template>
  <q-layout view="lHh Lpr lFf">
    <q-page-container >
      <router-view  />
    </q-page-container>
  </q-layout>
</template>

<script>
import { defineComponent, ref } from 'vue'

export default defineComponent({
  name: 'MainLayout',

  components: {},

  setup() {
    const leftDrawerOpen = ref(false)

    return {
    }
  }
})
</script>

<style>
@import url('https://fonts.googleapis.com/css2?family=Spline+Sans+Mono:ital,wght@0,300;0,400;0,500;0,600;0,700;1,300;1,400;1,500;1,600;1,700&display=swap');

::-webkit-scrollbar {
  display: none;
}


.titleFont {
  font-family: 'Spline Sans Mono', monospace;
}

* {
  padding: 0;
  margin: 0;
}
</style>
