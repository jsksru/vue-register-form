<template>
  <h2>
    <slot></slot>
  </h2>
</template>

<script>
export default {
  name: 'Title',
}
</script>

<style lang="scss" scoped>
@import '../styles/vars.scss';

h2 {
  margin: 0;
  font-size: $size-normal-text;
  font-weight: 400;
  color: $color-text-active;
}
</style>