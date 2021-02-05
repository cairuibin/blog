<template>
  <div class="MainNav">
    <div class="scroll_wrap">
      <ul class="ul">
        <li v-for="v in navTags" :key="v.id">{{ v.text }}</li>
      </ul>
    </div>
  </div>
</template>

<script>
import { navTags } from "../config/index";
export default {
  data() {
    return {
      navTags,
    };
  },
};
</script>

<style lang="scss" scoped>
.MainNav {
  max-width: 960px;
  height: 100%;
  margin: auto;
  > .scroll_wrap {
    height: 100%;
    overflow-x: auto;
    > .ul {
      min-width: 520px;
      height: 100%;
      display: flex;
      justify-content: space-between;
      align-items: center;
      font-size: 14px;
      width: auto;
      overflow-x: auto;
      > li {
        cursor: pointer;
      }
    }
  }
}

@media screen and (min-width: 10px) and (max-width: 550px) {
  .scroll_wrap::-webkit-scrollbar {
    width: 10px; 
    height: 5px;
  }
  .scroll_wrap::-webkit-scrollbar-thumb {
   border-radius: 10px;
    background-color: #3e78ed;
    background-image: -webkit-linear-gradient(
      45deg,
      rgba(255, 255, 255, 0.2) 25%,
      transparent 25%,
      transparent 50%,
      rgba(255, 255, 255, 0.2) 50%,
      rgba(255, 255, 255, 0.2) 75%,
      transparent 75%,
      transparent
    );
  }
  .scroll_wrap::-webkit-scrollbar-track {
    -webkit-box-shadow: inset 0 0 5px#3e78ed;
    border-radius: 10px;
    background: #ededed;
  }
}
</style>