<template>
<div id="app">
  <el-row :gutter="5">
    <el-col :span="4">
      <div class="grid-content bg-purple">
        <el-menu default-active="1-4-1" class="el-menu-vertical-demo" @open="handleOpen" @close="handleClose" :collapse="isCollapse">
          <el-submenu index="1">
            <template slot="title">
      <i class="el-icon-message"></i>
      <span slot="title">导航一</span>
</template>
    <el-menu-item-group>
      <el-menu-item index="1-1">选项1</el-menu-item>
      <el-menu-item index="1-2">选项2</el-menu-item>
    </el-menu-item-group>
  </el-submenu>
  <el-menu-item index="2">
    <i class="el-icon-menu"></i>
    <span slot="title">
        <router-link to="/index">表单</router-link>
    </span>
  </el-menu-item>
  <el-menu-item index="3">
    <i class="el-icon-setting"></i>
    <span slot="title">
      <router-link to="/table">表格</router-link>
    </span>
  </el-menu-item>
</el-menu>
      </div>
    </el-col>
    <el-col :span="20">
      <div class="grid-content bg-purple">
        <transition name="el-zoom-in-top" mode="out-in">
            <router-view></router-view>
        </transition>
      </div>
    </el-col>
  </el-row>
</div>
</template>

<script>
export default {
  data() {
    return {
      isCollapse: false
    };
  },
  methods: {
    handleOpen(key, keyPath) {
      console.log(key, keyPath);
    },
    handleClose(key, keyPath) {
      console.log(key, keyPath);
    }
  }
}
</script>

<style>
.grid-content {
  border-radius: 4px;
  min-height: 36px;
}

.component-fade-enter-active,
.component-fade-leave-active {
  transition: opacity .2s ease;
}

.component-fade-enter,
.component-fade-leave-to
/* .component-fade-leave-active for below version 2.1.8 */

{
  opacity: 0;
}
</style>
