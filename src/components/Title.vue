<template>
  <h1>
    <slot></slot>
  </h1>
</template>

<script>
export default {
  name: 'Title',
}
</script>

<style lang="scss" scoped>
@import '../styles/vars.scss';

h1 {
  margin: 0;
  font-size: $size-title-text;
  font-weight: 600;
  color: $color-title;
  margin-bottom: 8px;
}
</style>