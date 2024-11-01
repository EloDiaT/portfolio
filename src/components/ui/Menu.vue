<template>
  <nav class="Menu">
    <a :href="`#menu${index}`" class="Menu_item" v-for="(item, index) in menuItem" :key="index">
      <span>{{ item }}</span>
    </a>
  </nav>
</template>

<script setup lang="ts">
  const menuItem:String[] = [
    'Обо мне',
    'Опыт работы',
    'Проекты'
  ]

</script>

<style lang="scss">
.Menu {
  max-width: $menuWidth;
  width: 100%;
  @media all and (max-width: 768px) {
    display: flex;
    align-items: center;
    justify-content: space-between;
  }
  .Menu_burger {
    display: none;
    @media all and (max-width: 768px) {
      display: block;
    }
    span {
      display: block;
      width: 2.8em;
      height: .2em;
      background-color: $white
    }
  }
  .Menu_item {
    display: flex;
    align-items: center;
    justify-content: start;
    padding: 1.2em 0;
    text-decoration: none;
    
    &::before {
      display: inline-block;
      content: '';
      background-color: $colorText;
      width: 2.8em;
      height: .1em;
      margin-right: 1.6em;
      transition: $mainAnimStyleEase;
      @media all and (max-width: 768px) {
        content: none;
      }
    }
    span {
      cursor: pointer;
      color: $colorText;
      @extend .font-m;
      transition: $mainAnimStyle;
      font-weight: $medium;
    }
    &:hover {
      &::before {
        background-color: $white;
        width: 3.8em;
      }
      span {
        color: $white;
        animation: none;
      }
    }
  }
}
</style>