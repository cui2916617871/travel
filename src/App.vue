<template>
  <div id="app">
    <!-- 排除Detail组件，不被缓存，用到组件名字 -->
    <keep-alive exclude="Detail">
      <router-view/>
    </keep-alive>
  </div>
</template>

<script>
export default {
  name: 'App'
}
</script>

<style>
</style>
