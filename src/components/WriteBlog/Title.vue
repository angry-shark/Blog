<template>
  <div class="titleWrapper wrapper">
    <input
      type="text"
      class="blogTitle"
      v-model="title"
    >
  </div>
</template>
<script>
export default {
  data(){
    return {
      title: ''
    }
  }
}
</script>
<style lang="scss">
$font-size-b: 26px;
input.blogTitle {
  font-size: $font-size-b;
  border-bottom: 2px solid rgb(217, 217, 217);
}
input.blogTitle:focus {
  outline: none;
}
</style>

