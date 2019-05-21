<template>
  <div class="descript">
    <span class="descriptTitle">
      <slot name="title"></slot>
    </span>
    <p class="descriptP">
      <slot name="descript"></slot>
    </p>
  </div>
</template>
<style lang="scss">
.descript {
  white-space: nowrap; /*不分行显示*/
  overflow-x: hidden; /*溢出隐藏*/
  text-overflow: ellipsis; /*文字溢出省略号*/
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

