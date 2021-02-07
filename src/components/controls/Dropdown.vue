<template>
<div>
  <label>
    <span>{{title}}</span>
    <input :type="type" :placeholder="placeholder"/>
  </label>
  <span class="error" v-if="error">{{error}}</span>
</div>
</template>

<script>
export default {
  name: 'TextField',
  props: {
    title: String,
    placeholder: String,
    type: String,
    error: String,
  }
}
</script>

<style lang="scss" scoped>
@import '../../styles/vars.scss';

div {
  display: flex;
  flex-direction: column;
  gap: 8px;
}

label {
  display: flex;
  flex-direction: column;
  gap: 8px;

  span {
    font-size: $size-normal-text;
    font-weight: 500;
    color: $color-text;
  }
}

span.error {
  font-size: $size-small-text;
  color: $color-danger;
}

input {
  box-sizing: border-box;
  border: 1px solid $color-border;
  border-radius: $size-radius;
  color: $color-text-active;
  font-size: $size-normal-text;
  padding: 16px;
  outline: none;
  box-shadow: 0 4px 8px 0px rgba($color-title, 0.04);
  &::placeholder {
    color: $color-primary-light;
  }
  &:focus {
    border: 2px solid $color-primary;
    padding: 15px;
  }
}
</style>