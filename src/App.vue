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
import Header from "./views/Header";
import BlogList from "./views/BlogList";
import WriteBlog from "./views/WriteBlog";
export default {
  components: {
    "n-header": Header,
    "n-blog-list": BlogList,
    "n-write-blog": WriteBlog
  }
};
</script>

<style lang="scss">
$font-size-n: 18px;

* {
  box-sizing: border-box;
}
html,
body,
#app {
  height: 100%;
}
body {
  margin: 0;
  padding: 0;
}
input,
textarea {
  overflow-y: auto;
  width: 100%;
  color: rgb(89, 89, 89);
  border: none;
  padding: 20px 30px 20px 30px;
  font-size: $font-size-n;
  font-family: -apple-system, SF UI Text, Arial, PingFang SC, Hiragino Sans GB,
    Microsoft YaHei, WenQuanYi Micro Hei, sans-serif;
}
textarea {
  resize: none;
}
#app {
  display: flex;
  flex-direction: column;
}
.blogShow {
  display: flex;
  flex-grow: 1;
}
</style>
