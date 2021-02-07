<template>
  <button v-bind="$props">
    <slot></slot>
  </button>
</template>

<script>
export default {
  name: 'Button',
}
</script>

<style lang="scss" scoped>
@import '../../styles/vars.scss';

button {
  cursor: pointer;
  outline: none;
  font-family: inherit;
  box-sizing: border-box;
  background-color: $color-primary;
  border: none;
  border-radius: $size-radius;
  font-size: $size-normal-text;
  font-weight: 500;
  color: $color-light-bg;
  padding: 19px 38px;
  box-shadow: 0 2px 4px 0px rgba($color-title, 0.08),
              0 4px 8px 0px rgba($color-title, 0.08);
  &:hover {
    box-shadow: 0 12px 24px 0px rgba($color-title, 0.08),
                0 24px 48px 0px rgba($color-title, 0.16);
  }
  &:focus,
  &:active {
    border: 2px solid rgba($color-title, 0.86);
    padding: 17px 36px;
    box-shadow: 0 2px 4px 0px rgba($color-title, 0.01),
                0 4px 8px 0px rgba($color-title, 0.08);
  }
  &:disabled {
    cursor: not-allowed;
    box-shadow: 0 4px 8px 0px rgba($color-title, 0.08);
    background-color: $color-disabled-bg;
    color: $color-title;
  }
}
</style>