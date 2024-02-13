<script>
export default {
  name: 'App',
  methods: {
    openImporter(importerKey) {
      window.usecsv({
        importerKey,
        user: { userId: 123 },
        metadata: { anotherId: 12345 },
        batchSize: 1000,
        onData: (data) => console.log({ data })
      })
    }
  }
}
</script>

<template>
  <h1>UseCSV example in Vue.js</h1>
  <button class="btn" @click="openImporter('e3033735-73be-498a-9d3c-0a8b4c070e67')">
    Import Data
  </button>
  <!-- required div with id="usecsv-importer-root" -->
  <div id="usecsv-importer-root"></div>
</template>

<style scoped>
.btn {
  width: 170px;
  height: 70px;
  color: #fff;
  background-color: #027ad6;
  box-shadow: 0 32px 64px rgba(0, 0, 0, 0.07);
  font: 700 24px sans-serif;
  text-align: center;
  border: none;
  border-radius: 3px;
  cursor: pointer;
}
</style>
