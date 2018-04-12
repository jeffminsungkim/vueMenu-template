<template>
  <div class="navWrapper">
    <div id="menu" :class="{ active: isActive }">
      <el-menu mode="horizontal" @select="handleSelect" :router="true">
      <el-menu-item id="logo" index="/" :route="{ name: 'Root'}">
        <logo></logo>
      </el-menu-item>
      <el-menu-item index="/hello" :route="{ name: 'Hello' }">
        Hello
      </el-menu-item>
      <el-menu-item index="/projects" :route="{ name: 'Projects' }">
        Projects
      </el-menu-item>
      <el-menu-item index="/about" :route="{ name: 'About' }">
        About
      </el-menu-item>
      <el-menu-item index="/contact" :route="{ name: 'Contact' }">
        Contact
      </el-menu-item>
      </el-menu>
    </div>
    <div id="toggle" @click="select()">
      <div class="span" id="top" :class="{ active: isActive }"></div>
      <div class="span" id="middle" :class="{ active: isActive }"></div>
      <div class="span" id="bottom" :class="{ active: isActive }"></div>
    </div>
  </div>
</template>

<script>
import Logo from '@/components/Logo'

export default {
  components: {
    Logo
  },

  data() {
    return {
      activeIndex: '/hello',
      isActive: false
    }
  },
  methods: {
    handleSelect(key, keyPath) {
      console.log(key, keyPath);
    },
    select: function() {
      this.isActive = !this.isActive;
    }
  }
}
</script>
