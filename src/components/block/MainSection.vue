<template>
  <section :class="[{'MainSection_indentation': showIndentation}, 'MainSection']">
    <div class="MainSection_title" v-if="showTitle">
      <span>
        {{ title }}
      </span>
    </div>
    <slot/>
  </section>
</template>

<script setup lang="ts">
  interface poprsType {
    title?: string,
    showTitle?: boolean
    showIndentation?: boolean
  }
  defineProps({
    title: {
      type: String,
      default: ''
    }, 
    showTitle: {
      type: Boolean,
      default: false
    },
    showIndentation: {
      type: Boolean,
      default: false
    }
  }) as poprsType
</script>

<style lang="scss" scoped>
.MainSection_indentation {
  margin-top: $sectionIndentation;
}
.MainSection {
  .MainSection_title {
    position: sticky;
    top: -1.6em;
    z-index: 3;
    width: 100%;
    height: 4em;
    background-color: $bg;
    span {
      font-weight: $semibold;
      color: $white;
      @extend .font-b;
    }
  }
}
</style>