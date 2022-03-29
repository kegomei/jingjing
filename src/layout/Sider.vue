<template>
  <el-menu
          default-active="2"
          class="menu"
          :collapse="false"
          @open="handleOpen"
          @close="handleClose"
  >
    <el-menu-item index="1">
      <template #title>
        <el-icon size="18" class="mb4"><HomeFilled></HomeFilled></el-icon>
        <span class="ml4">系统首页</span>
      </template>
    </el-menu-item>
    <el-submenu index="2">
      <template #title>
          <el-icon size="18" class="mb4"><Setting></Setting></el-icon>
          <span class="ml4">系统管理</span>
      </template>
      <el-menu-item-group>
        <el-menu-item index="2-1" class="subItem">
          <el-icon size="14" class="mb8"><UserFilled></UserFilled></el-icon>
          角色权限
        </el-menu-item>
        <el-menu-item index="2-2" class="subItem">
          <el-icon size="14" class="mb8"><User></User></el-icon>
          用户管理
        </el-menu-item>
      </el-menu-item-group>
    </el-submenu>
    <el-submenu index="3">
      <template #title>基础信息</template>
      <el-menu-item index="3-1" class="subItem">物料分类</el-menu-item>
      <el-menu-item index="3-2" class="subItem">物料基本信息</el-menu-item>
      <el-menu-item index="3-3" class="subItem">料箱基础信息</el-menu-item>
      <el-menu-item index="3-4" class="subItem">空箱出入库</el-menu-item>
    </el-submenu>
    <el-submenu index="4">
      <template #title>入库管理</template>
      <el-menu-item index="4-1" class="subItem">物料入库</el-menu-item>
      <el-menu-item index="4-1" class="subItem">入库查阅</el-menu-item>
    </el-submenu>
    <el-submenu index="5">
      <template #title>Navigator Four</template>
    </el-submenu>
  </el-menu>
</template>

<script lang="ts">
  import {Options, Vue} from 'vue-class-component';
  import {
    Document,
    Menu as IconMenu,
    Location,
    Setting,
    HomeFilled,
    UserFilled,
    User
  } from '@element-plus/icons-vue'

  @Options({
    components: {
      Setting,
      HomeFilled,
      UserFilled,
      User
    },
    data: () => {
      return {
        menuConfig: [
        ]
      }
    },
    methods: {
      handleOpen: (key: string, keyPath: string[]) => {
        console.log(key, keyPath)
      },
      handleClose: (key: string, keyPath: string[]) => {
        console.log(key, keyPath)
      }
    }
  })
  export default class Sider extends Vue {
    handleOpen!: (key: string, keyPath: string[]) => void;
    handleClose!: (key: string, keyPath: string[]) => void;

  }
</script>

<style scoped lang="less">
  .el-menu-vertical-demo:not(.el-menu--collapse) {
    width: 200px;
    min-height: 400px;
  }
  .menu {
    width: 200px;
  }
  .subItem {
    text-align: left;
    padding-left: 80px !important;
    font-size: 12px;
  }
  .itemWrapper {
    display: flex;
    align-items: center;
  }
  .ml4 {
    margin-left: 4px;
  }
  .mb8{
    margin-bottom: 8px;
  }
  .mb4 {
    margin-bottom: 4px;
  }

</style>
