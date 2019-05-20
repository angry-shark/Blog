<template>
  <button
    class="commit"
    @click.prevent="$emit('commit')"
  >Commit</button>
</template>
<style lang="scss">
button.commit {
  border: none;
  background-color: rgb(236, 114, 89);
  width: 80px;
  padding: 10px 6px;
  color: white;
  cursor: pointer;
  border-radius: 16px;
  position: absolute;
  right: 25px;
  bottom: 0;
}
button.commit:focus {
  outline: none;
}
</style>
