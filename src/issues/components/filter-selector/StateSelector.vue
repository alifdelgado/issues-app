<script setup lang="ts"></script>

<template>
  <q-btn-toggle
    toggle-color="primary"
    push
    spread
    :options="[
      { label: 'All', value: 1 },
      { label: 'Open', value: 2 },
      { label: 'Closed', value: 3 },
    ]"
  />
</template>

<style scoped></style>
