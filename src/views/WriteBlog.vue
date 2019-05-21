<template>
  <div class="writeBlog">
    <n-title ref="title"></n-title>
    <n-content ref="content"></n-content>
    <n-commit-button @commit="postBlog()"></n-commit-button>
  </div>
</template>
<script>
import CommitButton from "../components/WriteBlog/CommitButton";
import Content from "../components/WriteBlog/Content";
import Title from "../components/WriteBlog/Title";
import global from "../Global";
import eventBus from '../eventBus.js'
export default {
  components: {
    "n-title": Title,
    "n-content": Content,
    "n-commit-button": CommitButton
  },
  data() {
    return {
      article: {
        title: "",
        content: ""
      }
    };
  },
  methods: {
    postBlog() {
      var blog = global.AV.Object.extend("blog");
      var blogData = new blog();
      blogData
        .save({
          title: this.$refs.title.title,
          body: this.$refs.content.content
        })
        .then(function(object) {
          alert("发布文章成功！");
          location.reload();
        });
    }
  },
  created() {
    eventBus.$on("getBlogData", (title, content) => {
      this.article.title = title;
      this.article.content = content;
      this.$refs.title.title = title;
      this.$refs.content.content = content;
    });
  }
};
</script>
<style lang="scss">
$shadow: inset 0 1px 2px rgba(27, 31, 35, 0.075);
$shadow-focus: inset 0 1px 2px rgba(27, 31, 35, 0.075),
  0 0 0 0.2em rgba(3, 102, 214, 0.3);
$indent: 0.5em;
.wrapper {
  display: flex;
  flex-direction: column;
  justify-content: center;
}
.writeBlog {
  flex-grow: 1;
  display: flex;
  flex-direction: column;
}
</style>

