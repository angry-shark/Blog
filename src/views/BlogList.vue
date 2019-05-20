<template>
  <div class="blogList">
    <ul>
      <li v-for="(blog, index) in blogArr" :key="index">{{ blog }}</li>
    </ul>
  </div>
</template>
<script>
import global from "../Global";
export default {
  data(){
    return {
      blogArr: []
    }
  },
  mounted() {
    var query = new global.AV.Query("blog");
    query.include("blog");
    query
      .find()
      .then((data)=> {
        this.blogArr = data;
      })
      .catch(function(error) {
        alert(JSON.stringify(error));
      });
  }
};
</script>
<style lang="scss">
.blogList {
  width: 300px;
  height: 100%;
  overflow-y: scroll;
}
</style>
