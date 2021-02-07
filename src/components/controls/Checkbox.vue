<template>
<div>
  <label>
    <input type="checkbox" :checked="checked"/>
    <span>
      <slot></slot>
    </span>
  </label>
</div>
</template>

<script>
export default {
  name: 'Checkbox',
  props: {
    checked: Boolean,
  }
}
</script>

<style lang="scss" scoped>
@import '../../styles/vars.scss';
</style>