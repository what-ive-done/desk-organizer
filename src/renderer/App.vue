<template>
  <div id="app">
    <div id="app-tile" class="tile is-ancestor">
      <div id="app-sidebar" class="tile is-parent">
        <sidebar />
      </div>
      <div id="app-main" class="tile is-parent is-8">
        <article class="tile is-child box">
          <router-view />
        </article>
      </div>
    </div>
  </div>
</template>

<script>
import Sidebar from '@/components/Sidebar/Index.vue'

export default {
  name: 'desk-organizer',
  components: {
    Sidebar
  }
}
</script>

<style>
/* CSS */
html, body, #app, #app-tile {
  width: 100vw;
  height: 100%;
  min-height: 100%;
  overflow: hidden;
}

#app-tile {
  margin: 0;
  padding: 0;
}
#app-tile .tile.is-parent {
  padding: 0.25rem;
}

#app-sidebar, #app-main {
  min-height: 100%;
  overflow: auto;
}
</style>
