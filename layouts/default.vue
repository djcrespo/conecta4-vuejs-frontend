<template>
  <div>
  <b-navbar>
    <template #brand>
      <b-navbar-item tag="router-link" :to="{ path: '/' }">
        <img src="~assets/connect4-logo.png" alt="Conecta 4">
      </b-navbar-item>
    </template>

    <template #end>
      <b-navbar-item tag="router-link" :to="{ path: '/' }">
        Inicio
      </b-navbar-item>
      <b-navbar-item tag="router-link" :to="{ path: '/score' }">
        Puntuación global
      </b-navbar-item>
    </template>
  </b-navbar>

    <section class="main-content columns">
      <div class="container column is-8 is-offset-2">
        <Nuxt />
      </div>
    </section>

  </div>
</template>

<script>
import { customIconConfig } from '../utils/icons'

export default {
  name: 'DefaultLayout',
  created () {
    this.$buefy.config.setOptions(customIconConfig)
  }
}
</script>
