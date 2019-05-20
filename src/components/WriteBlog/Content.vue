<template>
  <div class="containWrapper wrapper">
    <textarea
      cols="30"
      rows="10"
      v-model="content"
    ></textarea>
  </div>
</template>
<script>
export default {
  data(){
    return {
      content: ''
    }
  }
}
</script>

<style lang="scss">
.containWrapper {
  flex-grow: 1;
  textarea:focus {
    outline: none;
  }
  textarea {
    height: 100%;
    line-height: 1.8em;
    flex-grow: 1;
  }
}
</style>

