<template>
  <main class="MainLayout">
    <div class="MainLayout_wrapper">
      <div class="MainLayout_wrapper_fixed">
        <AboutMe
          :name="'Дмитрий'"
          :profession="'Middle Frontend Developer'"
          :description="''"
        >
          <template v-slot:description>
            <p>
              Я создаю интерфейсы для <br>
              Web - приложений и не только.
            </p>
          </template>
        </AboutMe>
        <div class="MainLayout_wrapper_fixed_nav">
          <MainSection class="MainLayout_wrapper_fixed_nav--menu">
            <Menu/>
          </MainSection>
          <MainSection class="MainLayout_wrapper_fixed_nav--social">
            <Social
              :arr="socilArr"
            />
          </MainSection>
        </div>
      </div>
      <div class="MainLayout_wrapper_scroll">
        <ViewScroll/>
        <MainSection 
          id="menu0"
          :title="'Обо мне'"
          :show-title="true"
          :show-indentation="false"
        >
          <TextArea>
            Фронтенд-разработчик с 2.8 годами коммерческого опыта  <br> и 3.8 годами работы в индустрии.<br><br>
            Специализируюсь на разработке интерфейсов с использованием <a class="link" href="https://vuejs.org/">Vue.js</a>  в стиле <a class="link" href="https://htmlacademy.ru/blog/css/pixel-perfect">pixel-perfect</a>, а также имею опыт в создании <br> 
            <a class="link" href="https://wordpress.com/ru/">WordPress-приложений</a> и реализации <a class="link" href="https://skillbox.ru/media/design/ux_ui_dizayn_chto_eto_takoe/">UI/UX</a> для финансовых и корпоративных систем.
            <br>
            <br>
    
            Основные достижения:
            <br>
            <br>
            <ul class="MainLayout_wrapper_scroll--ul">
              <li>Финансовое приложение <a class="link" href="https://vuejs.org/">(Vue.js)</a>: <br> разработка интерфейса и логики с нуля.</li>
              <br>
              <li>Админ-панель для телефонии <a class="link" href="https://vuejs.org/">(Vue.js)</a>: <br> реализация черного и белого списков для управления контактами.</li>
              <br>
              <li>HTML-креативы: <br> разработка адаптивных HTML-креативов для различных площадок.</li>
              <br>
              <li>Система синтеза речи: <br> создание <a class="link" href="https://tomoru.ru/media/speech-synthesis">TTS</a> для автоматического озвучивания текста.</li>
              <br>
              <li>Миграция алгоритма с <a class="link" href="https://ru.wikipedia.org/wiki/Visual_Basic_for_Applications">VBA</a> на <a class="link" href="https://nodejs.org/en">Node.js</a>: <br> повышение производительности парсинга документов.</li>
            </ul>
            <br>
            Способен эффективно работать как над отдельными модулями, так и над комплексными проектами.
          </TextArea>
        </MainSection>
        <MainSection 
          id="menu1"
          :title="'Опыт работы'"
          :show-title="true"
          :show-indentation="true"
        >
         <Card
            :link="'https://rednosed.agency/'"
            :title="'Системы Информационной Безопасности'"
            :subtitle="'Middle Frontend Developer'"
            :list="['html', 'css', 'scss', 'js', 'php', 'laravel', 'WordPress', 'vuex / router', 'mySql', 'Docker', 'vue.js', 'blade', 'inertia.js']"
          >
          <template v-slot:content >
            <div class="MainLayout_wrapper_scroll--content">
              Май 2024<br>
              — Октябрь 2024
            </div>
          </template>
            <template v-slot:description>
              <span class="MainLayout_wrapper_scroll--text">
                Должностные обязанности:
              </span>
              <br>
              <ul class="MainLayout_wrapper_scroll--ul">
                <li>Разработка Торговой площадки - Разработка UI по макетам дизайнера и дальнейшая интеграция с Backend, исправление уже готового Frontend функционала;</li>
                <li>Разработка CMS Wordpress приложений;</li>
                <li>Доработка существующих web-приложений - Исправление ошибок в вёрстке наполнение контентом готовых сайтов на CMS Wordpress;</li>
                <li>Разработка HTML креативов.</li>
              </ul>
              <br>
              <br>
              <span class="MainLayout_wrapper_scroll--text">
                Достижения:
              </span>
              <br>
              <ul class="MainLayout_wrapper_scroll--ul">
                <li>Миграция алгоритма парсинга с VBA на Node.js: переписал алгоритм парсинга для анализа документов с VBA на Node.js. Этот алгоритм автоматизирует обработку документов для формирования рейтинговых отчётов на основе данных, что существенно повысило производительность и удобство работы с отчётностью.</li>
                <li>Разработка WordPress-тем и приложений: создавал WordPress-темы и приложения в стиле pixel-perfect на основе предоставленных макетов, обеспечивая точное соответствие дизайну на всех этапах реализации.</li>
                <li>Разработка HTML-креативов: самостоятельно разработал HTML-креативы для более чем 15 площадок, таких как Avito и Sport.ru, точно следуя их техническим требованиям и стандартам.</li>
              </ul>
            </template>
          </Card>
         <Card
            :link="'https://smartstart24.ru/'"
            :title="'ООО Смарт Старт'"
            :subtitle="'Middle Frontend Developer'"
            :list="['html', 'css', 'scss', 'js', 'php', 'laravel', 'vuex / router', 'mariaDB', 'Docker', 'vue.js']"
          >
          <template v-slot:content >
            <div class="MainLayout_wrapper_scroll--content">
              Апрель 2024<br>
              — Май 2024
            </div>
          </template>
            <template v-slot:description>
              <span class="MainLayout_wrapper_scroll--text">
                Должностные обязанности:
              </span>
              <br>
              <ul class="MainLayout_wrapper_scroll--ul">
                <li>Разработка Финансового приложения;</li>
                <li>Доработка Frontend приложения - исправления различных ошибок в вёрстке , и помощь Backend разработчикам с Frontend частью.</li>
              </ul>
              <br>
              <br>
              <span class="MainLayout_wrapper_scroll--text">
                Достижения:
              </span>
              <br>
              <ul class="MainLayout_wrapper_scroll--ul">
                <li>Фронтенд для финансового приложения: реализовал UI/UX для финансового приложения, точно воссоздав макет дизайнера в стиле pixel-perfect. Работа была выполнена в рамках изначально поставленной задачи, сосредоточенной на создании удобного интерфейса для дальнейшей интеграции</li>
              </ul>
            </template>
          </Card>
          <Card
            :link="'https://russkiedengi.ru/'"
            :title="'Русские Деньги'"
            :subtitle="'Middle Frontend Developer'"
            :list="['html', 'css', 'scss', 'js', 'vue.js', 'vuex / router', 'php', 'mySql', 'blade', 'node.js', 'WordPress', 'Socket.io']"
          >
          <template v-slot:content >
            <div class="MainLayout_wrapper_scroll--content">
              Декабрь 2021<br>
              — Апрель 2024
            </div>
          </template>
            <template v-slot:description>
              <span class="MainLayout_wrapper_scroll--text">
                Должностные обязанности:
              </span>
              <br>
              <ul class="MainLayout_wrapper_scroll--ul">
                <li>Разработка Финансового приложения на стеке ( Vue + Vuex/Router + Socket.io );</li>
                <li>Разработка системы синтеза речи для озвучивания текста;</li>
                <li>Разработка UI \ UX системы управления учетными записями;</li>
                <li>Разработка Админ панелей для телефонии на базе Asterisk;</li>
                <li>Доработка CRM на стеке ( php + blade ) - внедрение UI компонентов , исправление ошибок в вёрстке.</li>
              </ul>
              <br>
              <br>
              <span class="MainLayout_wrapper_scroll--text">
                Достижения:
              </span>
              <br>
              <ul class="MainLayout_wrapper_scroll--ul">
                <li>Финансовое приложение и редизайн сайта: разработал финансовое приложение с нуля, улучшив обработку финансовых данных компании; дополнительно провел полный редизайн официального сайта компании на WordPress, улучшив его пользовательский интерфейс.</li>
                <li>Система синтеза речи: cоздал TTS-систему (Text-to-Speech) для автоматического озвучивания текстов что повысило доступность сервисов компании.</li>
                <li>Система управления учетными записями: разработал систему на базе Jabber для управления и создания учетных записей что улучшило коммуникацию и интеграцию сотрудников.</li>
                <li>Админ-панель для телефонии: реализовал функцию черного и белого списков для управления телефонными контактами на базе Asterisk что упростило контроль за вызовами.</li>
                <li>Поддержка фронтенд-разработки: получил возможность напрямую обсуждать фронтенд-задачи с руководством за вклад в ключевые проекты, выполнял координацию задач в команде из четырёх человек.</li>
              </ul>
            </template>
          </Card>
          <Card
            :link="'#menu2'"
            :title="'Freelance'"
            :subtitle="'Верстальщик'"
            :list="['html', 'css', 'scss', 'js']"
          >
          <template v-slot:content >
            <div class="MainLayout_wrapper_scroll--content">
              Март 2021 — <br>
              Декабрь 2021
            </div>
          </template>
            <template v-slot:description>
              <ul class="MainLayout_wrapper_scroll--ul">
                <li>Вёрстка макетов Figma - Pixel Perfect;</li>
                <li>Тестирование и исправление чужой Вёрстки;</li>
                <li>js модули (Слайдеры, таблицы, ползунки и прочее UI).</li>
              </ul>
            </template>
          </Card>
        </MainSection>
        <MainSection 
          id="menu2"
          :title="'Проекты'"
          :show-title="true"
          :show-indentation="true"
        >
          <Card
            v-for="(item, index) in project"
            :key="index"
            :title="item.title"
            :list="item.list"
            :content="item.content"
            :link="item.link"
          />
        </MainSection>
      </div>
    </div>
  </main>
</template>

<script setup lang="ts">
  import AboutMe from '../ui/AboutMe.vue';
  import MainSection from '../block/MainSection.vue';
  import Menu from '../ui/Menu.vue';
  import Social from '../ui/Social.vue';
  import TextArea from '../ui/TextArea.vue';
  import Card from '../ui/Card.vue';
  import ViewScroll from '../ui/ViewScroll.vue';

  const socilArr:Array<{ name: string; link: string }> = [
    { name: 'telegram', link: 'https://t.me/EIoDiaT' },
    { name: 'gitHub', link: 'https://github.com/EloDiaT?tab=repositories' },
  ]
  interface projectType {
    title?:string
    list?: string[]
    content?:string
    link?:string
  }
  const project:projectType[] = [ 
    { link:'https://guardora.ai/', title: 'Guardora', list: ['html', 'css', 'less', 'js', 'php', 'wordPress', 'canvas',], content: 'guardora.png' },
    { link:'https://www.cfi24.ru/', title: 'Cfi24', list: ['html', 'css', 'js', 'php', 'wordPress', 'slide.js'], content: 'cf24.png' },
    { link:'https://cabinet.russkiedengi.ru/', title: 'Russkiedengi LK', list: ['vue.js', 'vuex / router', 'socket.io', 'scss', 'js'], content: 'RdLK.png' },
    { link:'https://russkiedengi.ru/', title: 'Russkiedengi Site', list: ['wordPress', 'php', 'js', 'css'], content: 'rdOfficial.png' },
    { link:'https://russkiedengi.ru/', title: 'Russkiedengi Service', list: ['vue.js', 'js', 'php', 'blade', 'scss'], content: 'rdService.png' },
    { link:'https://github.com/EloDiaT/prev_view', title: 'Примеры моего кода', list: ['vue.js', 'js'], content: 'git.png' },
  ]
</script>

<style lang="scss">
  .MainLayout {
    width: 100dvw;
    height: 100dvh;
    .MainLayout_wrapper {
      padding: 9.6em 9.6em 0 9.6em;
      margin: 0 auto;
      max-width: 128em;
      display: grid;
      grid-template-columns: minmax($menuWidth, 1fr) minmax($menuWidth, 54em);
      @media all and (max-width: 768px) {
        grid-template-columns: auto;
        padding: 1em 1em 0 1em;
      }
      height: 100%;
      gap: $standardIndentation;
      .MainLayout_wrapper_fixed {
        padding-bottom: 9.6em;
        position: relative;
        @media all and (max-width: 768px) {
          padding-bottom: 0;
        }
        .MainLayout_wrapper_fixed_nav {
          @media all and (max-width: 768px) {
            display: flex;
            flex-direction: column;
            justify-content: center;
          }
          &--menu {
            margin-top: 9.6em;
            @media all and (max-width: 768px) {
              order: 2;
              margin-top: $standardIndentation;
            }
          }
          &--social {
            position: absolute;
            bottom: 9.6em;
            @media all and (max-width: 768px) {
              margin-top: $standardIndentation;
              bottom: 0;
              position: static;
              
            }
          }
        }
        
      }
      .MainLayout_wrapper_scroll {
        border: .1em solid $greenBG;
        padding: 1.6em 1.6em 0 1.6em;
        overflow-x: scroll;
        -ms-overflow-style: none;
        scrollbar-width: none;
        scroll-behavior: smooth;
        &::-webkit-scrollbar {
          display: none;
        }
        &--text {
          @extend .font-m;
        }
        &--content  {
          @extend .font-ml;
        }
        &--ul {
          position: relative;
          left: 1.4em;
        }
      }
    }
  }
</style>