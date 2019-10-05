<template>
  <div class="container screen">
    <div>
      <div v-html="text"></div>
    </div>
  </div>
</template>

<script>
const getTitle = require("get-title-markdown");
export default {
  head() {
    return {title: this.title && (this.title + ' | Ubuntu 20.04') || 'Ubuntu 20.04'};
  },

  async asyncData ({params, app, redirect}) {
    try {
      const fileContent = await import(`~/md/${params.md}.md`);
      const attr = fileContent.attributes;
      const title = getTitle(fileContent.default);
      console.log(title);
      return {text: fileContent.default, title: title || params.md.replace('-', ' ')};
      console.log(fileContent);
    }catch(e) {
      console.log(e);
      redirect('/');
    }
      
      return {

      };
    },
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
