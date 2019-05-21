<template>
  <header class="siteHeader">
    <div class="siteHeaderL">
      <img
        src="../assets/logo.png"
        alt="logo"
      >
      <span>Vue Blog</span>
    </div>
    <div class="siteHeaderR">
      <div class="input">
        <input
          type="text"
          class="select"
        >
        <svg
          class="icon"
          aria-hidden="true"
        >
          <use xlink:href="#icon-fangdajing"></use>
        </svg>
      </div>
      <span>My Blog</span>
      <span>New</span>
    </div>
  </header>
</template>
<style lang="scss">
.siteHeader {
  font-size: 16px;
  padding: 0 20px;
  border-bottom: 1px solid rgb(240, 240, 240);
  display: flex;
  justify-content: space-between;
  align-items: center;
  .siteHeaderL {
    display: flex;
    align-items: center;
    img {
      width: 30px;
    }
    span {
      padding-left: 15px;
    }
  }
  .siteHeaderR {
    display: flex;
    align-items: center;
    div.input {
      margin-right: 30px;
      position: relative;
      .select {
        height: 30px;
        background-color: rgb(238, 238, 238);
        outline: none;
        border: none;
        border-radius: 20px;
        text-indent: 1em;
      }
      svg.icon {
        cursor: pointer;
        position: absolute;
        right: 10px;
        top: 50%;
        transform: translateY(-50%);
      }
    }

    span {
      display: block;
      padding: 15px;
      cursor: pointer;
    }
    span:hover {
      background-color: rgb(245, 245, 245);
    }
  }
}
</style>

