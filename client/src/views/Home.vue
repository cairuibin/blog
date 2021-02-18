<template>
  <div id="Home">
    <div class="header_wrap">
      <MainHeader />
    </div>
    <div class="header_nav">
      <MainNav />
    </div>
    <div class="main_wrap">
      <div class="cheildren_tag"></div>
      <div class="content">
        <div class="left">22121</div>
        <div class="right">
          <Right />
        </div>
      </div>
    </div>
  </div>
</template>


<script>
import MainHeader from "../components/MainHeader";
import MainNav from "../components/MainNav";
import Right from "../components/Right";

export default {
  components: {
    MainHeader,
    MainNav,
    Right,
  },
};
</script>

<style lang="scss">
#Home {
  min-height: 100%;
}
.header_wrap {
  background: #fff;
  border-bottom: 1px solid #f1f1f1;
  color: #909090;
  height: 4.4rem;
}
.header_nav {
  background: #fff;
  border-bottom: 1px solid #f1f1f1;
  color: #909090;
  height: 3.2rem;

  top: 0;
}
.main_wrap {
  max-width: 960px;
  margin: auto;
  min-height: calc(100vh - 61px);
  display: flex;
  width: 100%;
  margin-top: 10px;
  flex-direction: column;
  .cheildren_tag {
    height: 30px;
    background: #000;
  }
  .content {
    flex: 1;
    margin-top: 10px;
    display: flex;
    > .left {
      height: inherit;
      flex: 1;
      background: #fff;
    }
    > .right {
      margin-left: 15px;

      width: 240px;
    }
  }
}
@media screen and (min-width: 200px) and (max-width: 800px) {
  .main_wrap .right {
    display: none !important;
  }
}
</style>