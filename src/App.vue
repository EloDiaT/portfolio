<template>
  <MainLayout/> 
</template>

<script setup lang="ts">
  import MainLayout from './components/layout/MainLayout.vue';
  interface Item {
    title: string;
    description: string;
    subtitle: string;
    content: string;
    list: string[];
  }
  const arrr: Item[] = [
    {
      title: 'Верстальщик · Freelance',
      description: 'Разработка Web - приложений для внтуреней работы сотрудников, (Онлайн заявки, CRM). Разработка официального сайта компании на базе Wordpress.Разарботка личного кабинета Микрофинансовой организации',
      subtitle: 'Middle Developer',
      list: [
        'vue1ue', 'vue1', 'vue2', 'vue3'
      ],
      content: 'RdLK.png'
    },
    {
      title: 'Верстальщик · Freelance',
      description: 'Разработка Web - приложений для внтуреней работы сотрудников, (Онлайн заявки, CRM). Разработка официального сайта компании на базе Wordpress.Разарботка личного кабинета Микрофинансовой организации',
      subtitle: 'Middle Developer',
      list: [
        'vue', 'vue1', 'vue2', 'vue3'
      ],
      content: '2020-2022'
    }
  ]

</script>

<style lang="scss">

</style>
