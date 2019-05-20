<template>
  <div class="writeBlog">
    <div class="titleWrapper wrapper">
        <input
          type="text"
          class="blogTitle"
          v-model="article.title"
        >
    </div>
    <div class="containWrapper wrapper">
        <textarea
          cols="30"
          rows="10"
          v-model="article.content"
        ></textarea>
    </div>
  </div>
</template>
<script>
export default {
  data(){
    return {
      article: {
        title: '',
        content: ''
      }
    }
  }
};
</script>
<style lang="scss">
$shadow: inset 0 1px 2px rgba(27, 31, 35, 0.075);
$shadow-focus: inset 0 1px 2px rgba(27, 31, 35, 0.075),
  0 0 0 0.2em rgba(3, 102, 214, 0.3);
$indent: 0.5em;
$font-size-n: 18px;
$font-size-b: 26px;
.wrapper {
  display: flex;
  flex-direction: column;
  justify-content: center;
}
.writeBlog {
  flex-grow: 1;
  display: flex;
  flex-direction: column;
  input,
  textarea {
    color: rgb(89, 89, 89);
    border: none;
    padding: 20px 30px 20px 30px;
    font-size: $font-size-n;
    font-family: -apple-system,SF UI Text,Arial,PingFang SC,Hiragino Sans GB,Microsoft YaHei,WenQuanYi Micro Hei,sans-serif;
  }
  input.blogTitle {
    font-size: $font-size-b;
    border-bottom: 2px solid rgb(217,217,217);
  }
  input.blogTitle:focus {
    outline: none;
  }
  textarea {
  }
  textarea:focus {
    outline: none;
  }
}
</style>

