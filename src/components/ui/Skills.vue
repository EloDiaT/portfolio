<template>
  <div class="Skills">
    <span>
      {{ props.text }}
    </span>
  </div>
</template>

<script setup lang="ts">
const props = defineProps({
  text: {
    type: String,
    default: ''
  }
})
</script>

<style lang="scss">
.Skills {
  width: auto;
  display: inline-flex;
  align-items: end;
  justify-content: center;
  height: 3.2em;
  padding: .5em 1.2em;
  background: $greenBG;
  border-radius: 1.5em;
  text-align: center;
  color: $green;
  span {
    font-weight: $medium;
    @extend .font-m;
  }
}
</style>