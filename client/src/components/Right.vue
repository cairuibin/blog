<template>
  <div class="right_wrap">
    <ul>
      <li>哈哈哈</li>
      <li>哈哈哈</li>
      <li>哈哈哈</li>
    </ul>
  </div>
</template>

<script>
export default {};
</script>

<style lang="scss" scoped>
.right_wrap {
  height: 100%;
  width: 100%;

  > ul {
    height: 100%;
    width: 100%;
    display: flex;
    flex-direction: column;
    > li {
        flex: 1;
        background: #fff;
    }
    >li:nth-child(2){
        margin: 15px 0;
    }
  }
}
</style>