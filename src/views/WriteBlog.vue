<template>
  <div class="writeBlog">
    <label>
      标题
      <input
        type="text"
        class="blogTitle"
      >
    </label>
    <!--标题 内容-->
  </div>
</template>
<script>
export default {};
</script>
<style lang="scss">
.writeBlog {
  input.blogTitle {
    border: 1px solid #d1d5da;
    box-shadow: inset 0 1px 2px rgba(27, 31, 35, 0.075);
    border-radius: 4px;
    font-size: 16px;
    padding: 6px 8px;
  }
  input.blogTitle:focus {
    outline: none;
    border-color: #2188ff;
    box-shadow: inset 0 1px 2px rgba(27, 31, 35, 0.075),
      0 0 0 0.2em rgba(3, 102, 214, 0.3);
  }
}
</style>

