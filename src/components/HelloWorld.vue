<template>
  <div class="main">
    <ul id="menu">
      <li data-menuanchor="page1" class="active">
        <a @click="$refs.fullpage.api.moveSectionDown()" href="#page1">Section 1</a>
      </li>
      <li data-menuanchor="page2">
        <a href="#page2">Section 2</a>
      </li>
    </ul>
    <full-page ref="fullpage" :options="options" id="fullpage">
      <div class="section">First section</div>
      <div class="section">Second Section</div>
    </full-page>
  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  data() {
    return {
      options: {
        menu: '#menu',
        navigation: true,
        anchors: ['page1', 'page2'],
        sectionsColor: ['#41b883', '#ff5f45']
      },
      msg: "Welcome to Your Vue.js App"
    }
  }
}
</script>

<style scoped>
.main {
  border: 1px solid red;
}
</style>
