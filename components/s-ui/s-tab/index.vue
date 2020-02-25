<template>
  <div class="s-tab-wrap" :class="{'is-active':isActive}">
    <div class="s-tab-panel">
      <slot></slot>
    </div>
  </div>
</template>

<script>
export default {
  name: 's-tab',
  inject: ['$tabs'],
  props: {
    title: {
      type: String,
      default: ''
    }
  },
  computed: {
    isActive () {
      return this.$tabs.navList[this.$tabs.value].id === this.id;
    }
  },
  data () {
    return {
      id: 's-tab-id-' + Math.random().toString(36).substr(2)
    };
  },
  created () {
    const { id, title } = this;
    this.$tabs.navList = this.$tabs.navList.concat({ id, title });
  },
  beforeDestroy () {
    this.$tabs.navList = this.$tabs.navList.filter(item => item.id !== this.id);
  }
};
</script>

<style lang="scss">
.s-tab-wrap {
  width: 100%;
  flex-shrink: 0;
  box-sizing: border-box;
  height: 0;
  overflow: hidden;
  &.is-active {
    height: auto;
    overflow: visible;
  }
}
</style>
