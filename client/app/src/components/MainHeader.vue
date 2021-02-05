<template>
  <div class="MainHeader">
    <div class="logo">
      <img :src="Logo" alt="" />
    </div>
    <ul class="Headertabs_wrap">
      <li class="Headertabs_1">
        <ul class="Headertabs_content">
          <li v-for="v in tab_config" :key="v.id">{{ v.text }}</li>
        </ul>
      </li>
      <li class="search">
        <div class="input_wrap">
          <input type="text" placeholder="搜索文章" />
          <span class="icon">搜 索</span>
        </div>
      </li>
      <li class="edit">
        <button>写文章</button>
      </li>
      <li class="notice">
        <div class="notice_wrap">
          <span>通知</span>
          <span class="pos">11</span>
        </div>
      </li>
      <li class="avanter">
        <div class="img_wrap">
          <img :src="avanter" alt="" />
        </div>
      </li>
    </ul>
  </div>
</template>

<script>
import Logo from "../assets/logo.svg";
import avanter from "../assets/avanter.png";
import { tab_config } from "../config/index";
export default {
  data() {
    return {
      Logo,
      avanter,
      tab_config,
    };
  },
};
</script>

<style lang="scss" scoped>
.MainHeader {
  max-width: 960px;
  height: 100%;
  margin: auto;
  display: flex;
  justify-content: space-between;
  align-items: center;
  > .logo {
    width: 98px;
    height: 41px;
    cursor: pointer;
    > img {
      word-wrap: 100%;
      height: 100%;
      max-width: 100%;
      min-width: 100%;
    }
  }
  > .Headertabs_wrap {
    flex: 1;
    display: flex;
    align-items: center;
    height: 100%;
    > li {
      flex: 1;
      height: 100%;
      display: flex;
      align-items: center;
    }
    > .Headertabs_1 {
      display: flex;
      flex: 1.6;
      .Headertabs_content {
        flex: 1;
        display: flex;
        justify-content: space-around;
        font-size: 1.33rem;
        > li {
          flex: 1;
          display: flex;
          justify-content: space-around;
          cursor: pointer;
        }
      }
    }
    > li.search {
      cursor: pointer;
      flex: 1.3;
      > .input_wrap {
        position: relative;
        > input {
          padding-right: 48px;
          padding-left: 10px;
          height: 32px;

          border: 1px solid #ccc;
          color: #888;
          border-radius: 20px;
          box-sizing: border-box;
          outline: none;
        }
        > input:focus {
          border: 1px solid #3e78ed;
        }
        > input:focus + .icon {
          color: #3e78ed;
          font-weight: 500;
        }
        > input:focus + .icon::before {
          color: #3e78ed;
          font-weight: 300;
        }
        > .icon {
          position: absolute;
          right: 10px;
          top: 8px;
          color: #888;
          font-size: 14px;
        }
        > .icon::before {
          content: "|";
          font-size: 1.6rem;
          position: absolute;
          top: -5px;
          left: -8px;
          font-weight: 300;
          color: #ccc;
        }
      }
    }
    > li.edit {
      display: flex;
      align-items: center;
      justify-content: space-around;
      flex: 0.4;
      > button {
        box-sizing: border-box;
        cursor: pointer;
        height: 28px;
        padding: 0 10px;
        background: #3e78ed;
        color: #fff;
        outline: none;
        font-size: 14px;

        border-radius: 4px;
        border: 1px solid #3e78ed;
      }
      > button:hover {
        border: 1px solid #3e78ed;
        background: #3e78ed;
      }
    }
    > li.notice {
      cursor: pointer;
      display: flex;
      align-items: center;
      justify-content: space-around;
      flex: 0.4;
      > .notice_wrap {
        position: relative;
        display: flex;
        align-items: center;
        justify-content: space-around;
        width: 100%;
        height: 100%;
        font-size: 14px;
        max-width: 80px;
        > .pos {
          position: absolute;
          background: #f00;
          top: 13px;
          right: 11px;
          border-radius: 50%;
          color: #fff;
          padding: 2px;
          font-size: 12px;
        }
      }
    }
    > li.avanter {
      cursor: pointer;
      text-align: right;
      flex: 0.4;
      .img_wrap{
          width: 100%;text-align: right;
      }
    }
  }
}

@media screen and (min-width: 200px) and (max-width: 800px) {
  .Headertabs_1 {
    display: none !important;
  }
  .search {
    display: none !important;
  }
 
}
</style>