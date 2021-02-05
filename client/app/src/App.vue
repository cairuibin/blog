<template>
  <div id="app">
    <div id="_ruibin">
      <router-view />
    </div>
  </div>
</template>
<style lang="scss" >
* {
  margin: 0;
  padding: 0;
  list-style: none;
}
html{
  min-width: 231px;
}
html,
body,
#app,
#_ruibin {
  width: 100%;
  height: 100%;
  font-size: 12px;
  font-family: -apple-system, system-ui, Segoe UI, Roboto, Ubuntu, Cantarell,
    Noto Sans, sans-serif, BlinkMacSystemFont, "Helvetica Neue", "PingFang SC",
    "Hiragino Sans GB", "Microsoft YaHei", Arial;
  word-break: break-word;
  text-rendering: optimizeLegibility;
  color: #333;
  background-color: #f4f5f5;
}
</style>
