<template>
  <section class="home-box">
    <div class="side-logo">
      <transition enter-active-class="animate__animated animate__fadeInLeft">
        <span class="logo-title">VUE·ADMIN</span>
      </transition>
    </div>
    <div class="info-box">
      <p class="sub-title" style="font-weight: bold">本项目 基于 Vue 3 + JavaScript + Pinia +Vite + ElementPlus.</p>
      <p>本项目为一个现代化的管理后台模板，提供了一系列功能丰富的组件和工具，帮助开发者快速搭建和开发前后台管理应用。
        <br>
        对快速构建Vue3全栈项目有很大的帮助，解决每次新建项目基础配置的烦恼.
        <br>
        <p style="font-weight: bold">无论你是一个开发者寻找一个可靠的管理后台模板，还是一个学习者想要深入了解现代前端技术，
          VUE·ADMIN 都是一个非常有价值的项目。
          <br>
          因为它弥补了不习惯使用TypeScript开发的同学，使用JavaScript版本就能更快上手熟悉。</p>
        <p style="font-weight: bold;color: red"><a href="https://gitee.com/Z568_568/ZHOUYI-ADMIN.git" target="_blank">✌️项目如果对您有帮助，希望能得到您的 star 传送门✨</a></p>
      </p>
    </div>
   
    <div style="margin-top: 30px">
      <el-timeline style="max-width: 600px">
        <el-timeline-item
            v-for="(activity, index) in activities"
            :key="index"
            :icon="activity.icon"
            :type="activity.type"
            :color="activity.color"
            :size="activity.size"
            :hollow="activity.hollow"
            :timestamp="activity.timestamp"
        >
          {{ activity.content }}
        </el-timeline-item>
      </el-timeline>
    </div>
  </section>
</template>

<script setup>
import { MoreFilled } from '@element-plus/icons-vue'
import setting from '@/setting.js'
import { ZyMessage } from '@/utils/util.toast.js'

</script>


<style lang="scss" scoped>
.home-box {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  .info-box {
    font-size: 15px;
    color: #6c6c6c;
    text-align: center;
    line-height: 1.8;
  }

}
.side-logo {
  height: $navbar-height;
  line-height: $navbar-height;
  font-weight: bold;
  font-size: 50px;
  font-family: "Courier New";
  color: var(--el-color-primary);
  margin: 15px;
}
</style>
