<template>
    <b-navbar toggleable type="dark" variant="dark">
    <b-navbar-brand href="#" disabled>Quiz App</b-navbar-brand>

    <b-navbar-toggle target="navbar-toggle-collapse">
      <template v-slot:default="{ expanded }">
        <b-icon v-if="expanded" icon="chevron-bar-up"></b-icon>
        <b-icon v-else icon="chevron-bar-down"></b-icon>
      </template>
    </b-navbar-toggle>

    <b-collapse id="navbar-toggle-collapse" is-nav>
      <b-navbar-nav class="ml-auto">
        <b-nav-item disabled href="#">Counter:{{ numCorrect }}/{{ numTotal }}</b-nav-item>
      </b-navbar-nav>
    </b-collapse>
  </b-navbar>
</template>

<script>
export default {
  props: [
    'numCorrect',
    'numTotal'
  ]
}
</script>