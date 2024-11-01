<template>
    <div class="AboutMe">
      <h1 class="AboutMe--name">
        <span v-if="!$slots.title">{{ name }}</span>
        <slot v-else name="title"/>
      </h1>
      <h2 class="AboutMe--profession">
        <span v-if="!$slots.profession">{{ profession }}</span>
        <slot v-else name="profession"/>
      </h2>
      <div class="AboutMe--description">
        <p v-if="!$slots.description">
          {{ description }}
        </p>
        <slot v-else name="description"/>
      </div>
    </div>
</template>

<script setup lang="ts">
interface typeProps {
  name?: String
  profession?: String
  description?: String
}
defineProps({
  name: {
    type: String,
    default: ''
  },
  profession: {
    type: String,
    default: '',
  },
  description: {
    type: String,
    default: ''
  }
}) as typeProps
</script>

<style lang="scss">
  .AboutMe {
    max-width: $menuWidth;
    width: 100%;
    @media all and (max-width: 768px) {
      max-width: none;
    }
    &--name {
      span {
        @extend .font-big;
        color: $white;
        letter-spacing: -.025em;
        font-weight: $semibold;
      }
    }
    &--profession {
      margin-bottom: $littleIndentation;
      span {
        @extend .font-b;
        color: $white;
        font-weight: $medium;
        letter-spacing: -.025em;
      }
    }
    &--description {
      color: $colorText;
      @extend .font-m;
      font-weight: $medium;
    }
  }
</style>