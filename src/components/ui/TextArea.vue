<template>
  <div class="TextArea">
    <slot/>
  </div>
</template>

<style lang="scss">
.TextArea {
  @extend .font-m;
  color: $colorText;
  font-weight: $medium;
}
</style>