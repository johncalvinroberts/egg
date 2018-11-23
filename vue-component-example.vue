<style lang="scss" src="eggcss/components/modal.scss"></style>

<template>
  <div :class="['modal', activeClassName]">
    <slot/>
  </div>
</template>

<script>
export default {
  props: {
    active: {
      type: Boolean,
      default: false
    }
  },
  computed: {
      activeClassName () {
        return this.active ? 'active' : ''
      }
  }
}
</script>