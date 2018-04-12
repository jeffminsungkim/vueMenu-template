<template>
  <div class="app-wrapper">
  <navbar></navbar>
  <div class="main-container">
    <app-content></app-content>
  </div>
  </div>
</template>

<script>
import { Navbar, AppContent } from '@/views/layouts/components'

export default {
  name: 'AppLayout',
  components: {
    Navbar,
    AppContent
  }
}
</script>

<style rel="stylesheet/scss" lang="scss" scoped>
.app-wrapper {
  position: relative;
  height: 100%;
  width: 100%;
}
.main-container {
  text-align: center;
  margin-top: 400px;
  min-height: 50vh;
}
</style>
