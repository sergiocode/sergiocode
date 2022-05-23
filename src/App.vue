<template>
  
  <div id="app">
    <NavBar/>
    <ContentItem/>
  </div>

</template>

<script>
import NavBar from './components/NavBar.vue'
import ContentItem from './components/Content-Item.vue';

require('../src/assets/css/App.css');
require('../src/assets/css/styles.css');


export default {
  name: 'App',
  components: {
    NavBar,
    ContentItem
  }
}
</script>
