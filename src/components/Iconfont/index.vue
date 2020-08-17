// 分装iconfont小图标成为组件
<template>
  <svg class="svg-icon" aria-hidden="true">
    <use :xlink:href="iconName" />
  </svg>
</template>

<script>
import '@/assets/iconfont/iconfont'
export default {
  name: 'IconSvg',
  props: {
    iconClass: {
      type: String,
      required: true
    }
  },
  computed: {
    iconName() {
      return `#${this.iconClass}`
    }
  }
}
</script>

<style scoped>
  .svg-icon {
    width: 1.5em;
    height: 1.5em;
    vertical-align: -0.15em;
    fill: currentColor;
    overflow: hidden;
  }
</style>
