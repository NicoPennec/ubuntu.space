<template>
  <div class="container screen">
    <div>
      <h1>Links</h1>
      <h2>Official Ubuntu sites</h2>
      <ul>
        <li><a href="#" data-href="https://ubuntu.com" v-on:click="op">ubuntu.com</a> - Official Ubuntu website</li>
        <li><a href="#" data-href="https://canonical.com" v-on:click="op">canonical.com</a> - Official Canonical website</li>
        <li><a href="#" data-href="https://xubuntu.com" v-on:click="op">xubuntu.com</a> - Official xUbuntu website</li>
      </ul>
    </div>
  </div>
</template>

<script>
export default {
  head: {
    title: 'Links | Ubuntu 20.04'
  },
  methods: {
    op(op) {
      window.open(op.target.dataset.href);
    }
  }
}
</script>

<style>

.title {
  font-family: 'Quicksand', 'Source Sans Pro', -apple-system, BlinkMacSystemFont,
    'Segoe UI', Roboto, 'Helvetica Neue', Arial, sans-serif;
  display: block;
  font-weight: 300;
  font-size: 35px;
  color: #35495e;
  letter-spacing: 1px;
}

.subtitle {
  font-weight: 300;
  font-size: 48px;
  color: #526488;
  word-spacing: 5px;
  padding-bottom: 15px;
  padding-top: 48px;
}

.description {
    font-family: 'Quicksand', 'Source Sans Pro', -apple-system, BlinkMacSystemFont,
    'Segoe UI', Roboto, 'Helvetica Neue', Arial, sans-serif;
    padding: 15px;
}

.links {
  padding-top: 15px;
}

.authors {
  color: #448b00;
}
</style>
