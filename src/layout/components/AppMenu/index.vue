<template>
  <div class="app-menu">
    <el-menu
      active-text-color="#ffd04b"
      background-color="#545c64"
      class="el-menu-vertical-demo"
      default-active="2"
      text-color="#fff"
      @open="handleOpen"
      @close="handleClose"
      :collapse="$store.state.isCollapse"
      router
    >
      <el-menu-item index="/">
        <el-icon><House /></el-icon>
        <span>首页</span>
      </el-menu-item>
  
      <el-sub-menu index="1">
        <template #title>
          <el-icon><Guide /></el-icon>
          <span>权限管理</span>
        </template>
        <el-menu-item index="/permission/permission_admin">
          管理员
        </el-menu-item>
        <el-menu-item index="/permission/permission_role">
          角色
        </el-menu-item>
        <el-menu-item index="/permission/permission_rule">
          规则
        </el-menu-item>
      </el-sub-menu>
  
      <el-menu-item index="4">
        <el-icon><setting /></el-icon>
        <span>设置</span>
      </el-menu-item>
    </el-menu>
  </div>
</template>
    
  <script lang="ts" setup>
    import {
      House,
      Guide,
      Setting,
    } from '@element-plus/icons-vue'
  
    const handleOpen = (key: string, keyPath: string[]) => {
      console.log(key, keyPath)
    }
    const handleClose = (key: string, keyPath: string[]) => {
      console.log(key, keyPath)
    }
  </script>
  
  <style lang="scss" scoped>
  .app-menu {
      background-color: #545c64;
  }
  .el-menu {
      border-right: none;
  }
  .el-menu:not(.el-menu--collapse) {
    width: 200px;
    min-height: 400px;
  }
  </style>