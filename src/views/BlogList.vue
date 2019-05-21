<template>
  <div class="blogList">
    <ul>
      <li
        v-for="(blog, index) in blogArr"
        :key="index"
      >
        <n-icon></n-icon>
        <n-descript>
          <template v-slot:title>{{blog.attributes.title}}</template>
          <template v-slot:descript>{{blog.attributes.body}}</template>
        </n-descript>
      </li>
    </ul>
  </div>
</template>
<script>
import global from "../Global";
import Icon from "../components/BlogList/Icon";
import Descript from '../components/BlogList/Descript'
export default {
  components: {
    "n-icon": Icon,
    'n-descript': Descript
  },
  data() {
    return {
      blogArr: []
    };
  },
  mounted() {
    var query = new global.AV.Query("blog");
    query.include("blog");
    query
      .find()
      .then(data => {
        this.blogArr = data.reverse();
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
  li::before {
    position: absolute;
    content: "";
    display: block;
    flex-shrink: 0;
    width: 5px;
    height: 100%;
    background-color: rgb(64, 182, 130);
  }
  li {
    position: relative;
    display: flex;
    justify-content: space-between;
    align-items: center;
    height: auto;
    padding: 20px 0;
    border-bottom: 1px solid rgb(217, 217, 217);
  }
}
</style>
