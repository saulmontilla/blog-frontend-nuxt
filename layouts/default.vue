<template>
  <b-container fluid>
    <b-row>
      <sidebar-menu />

      <b-col class="main">
        <nuxt />
      </b-col>
    </b-row>
  </b-container>
</template>

<script>
import SidebarMenu from '../components/SidebarMenu'

export default {
  components: {
    SidebarMenu
  }
}
</script>

<style>
:root {
  --orange: #f56a6a;
  --dark-orange: #da4343;
}
body {
  color: #7f888f;
}
h1,h2,h3,h4,h5,h6 {
  color: #000;
}
h1 {
  font-size: 4rem;
}
h2 {
  font-size: 1.75rem;
}
h3 {
  font-size: 1.25rem;
}
.main {
    padding: 3rem 4rem 0 4rem;
  }
</style>