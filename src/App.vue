<template>
  <Sider></Sider>
  <RouterView></RouterView>
</template>

<script>
  import Sider from '@/layout/Sider'

export default {
  name: 'App',
  components: {
    Sider
  }
}
</script>

<style lang="less">
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
#app {
  height: 100%;
  display: flex;
  flex-direction: row;
  &::-webkit-scrollbar {
   width: 0 !important;
 }
}
</style>
