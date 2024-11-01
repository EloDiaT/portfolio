<template>
  <a :href="link" target="_blank" class="Card">
    <div class="Card_marker">
     <div class="Card_marker_template">
      <div v-if="!$slots.content">
        <img v-if="content && /\.(jpg|svg|png)$/i.test(content)" 
          :src="require(`@/assets/img/${content}`)" 
          :alt="content"
        >
        <span v-else>
          {{ content }}
        </span>
      </div>
      <slot v-else name="content"/>
     </div>
    </div>
    <div class="Card_content">
      <div> 
        <div class="Card_content--title" v-if="!$slots.title">
          <span>
            {{ title }} 
          </span>
          <svg v-if="showArrow" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 20 20" fill="currentColor" aria-hidden="true">
            <path fill-rule="evenodd" d="M5.22 14.78a.75.75 0 001.06 0l7.22-7.22v5.69a.75.75 0 001.5 0v-7.5a.75.75 0 00-.75-.75h-7.5a.75.75 0 000 1.5h5.69l-7.22 7.22a.75.75 0 000 1.06z" clip-rule="evenodd"/>
          </svg>
        </div>
        <slot v-else name="title"/>
      </div>
      <div> 
        <div class="Card_content--subtitle" v-if="!$slots.subtitle">
          <span>{{ subtitle }}</span>
        </div>
        <slot v-else name="subtitle"/>
      </div>
      <div class="Card_content--description">
        <div  v-if="!$slots.description">
          <span>
            {{ description }} 
          </span>
        </div>
        <slot v-else name="description"/>
      </div>
      <div>
        <div class="Card_content_list" v-if="!$slots.list">
          <Skills
            v-for="(item, index) in list"
            :key="index"
            :text="item"
          />
        </div>
        <slot v-else name="list"/>
      </div>
     
    </div>
  </a>
</template>

<script setup lang="ts">
  import { defineProps, computed } from 'vue';
  import Skills from './Skills.vue'
  interface TypeProps {
    title?: string;
    subtitle?: string;
    description?: string;
    list?: string[];
    content?: string;
    showArrow?: boolean;
    link?:string
  }
defineProps({
  title: {
    type: String,
    default: ''
  },
  subtitle: {
    type: String,
    default: ''
  },
  description: {
    type: String,
    default: ''
  },
  list: {
    type: Array as () => string[],
    default: () => []
  },
  content: {
    type: String,
    default: ''
  },
  link: {
    type: String,
    default: ''
  },
  showArrow: {
    type: Boolean,
    default: true
  }
}) as TypeProps;
</script>

<style lang="scss">
.Card {
  margin-top: $standardIndentation;
  display: grid;
  grid-template-columns: 15em 1fr;
  align-items: start;
  justify-content: start;
  transition: $mainAnimStyle;
  padding: 1.6em;
  max-width: 52.8em;
  width: 100%;
  height: auto;
  text-decoration: none;
  cursor: pointer;
  @media all and (max-width: 768px) {
    max-width: none;
  }
  .Card_marker {
    position: sticky;
    top: 3.3em;
    .Card_marker_template {
      img {
        margin-top: .6em;
        max-width: 12em;
        width: 100%;
        height: auto;
        border-radius: .5em;
      }
      font-weight: $medium;
      color: rgb(100 116 139 / 1);
      span {
        @extend .font-ml;
      }

    }
  }
  .Card_content {
    &--title {
      text-decoration: none;
      color: $white;
      letter-spacing: -.025em;
      font-weight: $medium;
      svg {
        width: 1.6em;
        height: 1.6em;
        transition: $mainAnimStyle;
        margin-left: 0.4em;
      }
      span {
        @extend .font-b;
      }
    }
    &--subtitle {
      margin-top: .8em;
      color: $colorText2;
      font-weight: $medium;
      span {
        @extend .font-m;
      }
    }
    &--description {
      margin-top: .8em;
      color: $colorText;
      font-weight: $medium;
      line-height: 1.5;
      span, li {
        @extend .font-ml;
      }
    }
    .Card_content_list {
      margin-top: .8em;
      & > div {
        margin-right: .8em;
        margin-bottom: .8em;
      }
    }
  }
  &:hover {
    background-color: rgba(148, 163, 184, 0.05);
    border-radius: 5px;
    .Card_content--title {
      color: $green;
      svg {
        fill: $green;
        transform: translate(2px,-2px);
      }
    }
  }
}
</style>