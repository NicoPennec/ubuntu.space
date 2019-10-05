<template>
<div class="template">
  <header>
    <b-navbar toggleable="lg" type="dark" variant="info" fixed="top">
      <b-navbar-brand href="/">Ubuntu 20.04</b-navbar-brand>

      <b-navbar-toggle target="nav-collapse"></b-navbar-toggle>

      <b-collapse id="nav-collapse" is-nav>
        <b-navbar-nav>
          <b-nav-item href="/19.10">19.10</b-nav-item>
          <b-nav-item href="/downloads">Downloads</b-nav-item>
          <b-nav-item href="/how-to">How to</b-nav-item>
          <b-nav-item href="/about">About</b-nav-item>
          <b-nav-item href="/links">Links</b-nav-item>
        </b-navbar-nav>
        <b-navbar-nav class="ml-auto">
        </b-navbar-nav>
      </b-collapse>
    </b-navbar>
  </header>
  <div class="content">
    <nuxt />
  </div>
  <footer class="bg-info">
    <div class="container footer-container">This site is not official. See&nbsp;<a href="/links">links</a>&nbsp;page.</div>
  </footer>
</div>
</template>

<style>


.screen {
  min-height: 100vh;
}

.content {
  padding-bottom: 30px;
  padding-top: 30px;
}

.bg-info {
  color: rgba(255, 255, 255, 200);
}

.bg-info a{
  color: rgba(255, 255, 255, 150);
}

footer {
  padding-top: 15px;
  padding-bottom: 15px;
}

body{
  padding-top: 60px;
}

html {
  font-family: 'Source Sans Pro', -apple-system, BlinkMacSystemFont, 'Segoe UI',
    Roboto, 'Helvetica Neue', Arial, sans-serif;
  font-size: 16px;
  word-spacing: 1px;
  -ms-text-size-adjust: 100%;
  -webkit-text-size-adjust: 100%;
  -moz-osx-font-smoothing: grayscale;
  -webkit-font-smoothing: antialiased;
  box-sizing: border-box;
}

*,
*:before,
*:after {
  box-sizing: border-box;
  margin: 0;
}

.button--green {
  display: inline-block;
  border-radius: 4px;
  border: 1px solid #3b8070;
  color: #3b8070;
  text-decoration: none;
  padding: 10px 30px;
}

.button--green:hover {
  color: #fff;
  background-color: #3b8070;
}

.button--grey {
  display: inline-block;
  border-radius: 4px;
  border: 1px solid #35495e;
  color: #35495e;
  text-decoration: none;
  padding: 10px 30px;
  margin-left: 15px;
}

.button--grey:hover {
  color: #fff;
  background-color: #35495e;
}
</style>
