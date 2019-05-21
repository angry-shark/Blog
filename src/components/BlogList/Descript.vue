<template>
  <div class="descript">
    <span class="descriptTitle">JSON详解</span>
    <p class="descriptP">这是一段描述描述这是一段描述描述这是一段描述描述这是一段描述描述这是一段描述描述这是一段描述描述</p>
  </div>
</template>
<style lang="scss">
.descript {
  .descriptTitle {
    color: #333;
    font-size: 18px;
  }
  .descriptP {
    color: #595959;
    font-size: 14px;
    margin: 10px 0;
    overflow: hidden;
    display: -webkit-box;
    -webkit-line-clamp: 1;
    -webkit-box-orient: vertical;
  }
}
</style>

