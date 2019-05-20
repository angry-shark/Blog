<template>
  <div id="app">
    <n-header></n-header>
    <main class="blogShow">
      <n-blog-list></n-blog-list>
      <n-write-blog></n-write-blog>
    </main>
  </div>
</template>
<script>
import Header from './views/Header'
import BlogList from './views/BlogList'
import WriteBlog from './views/WriteBlog'
export default {
  components: {
    'n-header': Header,
    'n-blog-list': BlogList,
    'n-write-blog': WriteBlog
  }
}
</script>

<style>
body {
  margin: 0;
  padding: 0;
}
input {
  border: none;
}
.blogShow {
  display: flex;
}
</style>
