<template>
  <f7-page name="help">
    <f7-navbar title="Допомога" back-link="Назад" />

    <div class="app-content">
      <div class="page-heading">
        <h1>Допомога</h1>
        <p>Як користуватися TaskFlow</p>
      </div>

      <div class="info-card">
        <h3>Головна сторінка</h3>
        <p>
          Переглядайте загальну кількість завдань,
          кількість виконаних і тих, що очікують виконання.
          Нижче розташований список останніх завдань.
        </p>
      </div>

      <div class="info-card">
        <h3>Список завдань</h3>
        <p>
          Відкрийте розділ «Завдання», щоб переглянути
          назви, описи та стан усіх завдань.
          Зелена позначка означає виконане завдання.
        </p>
      </div>

      <div class="info-card">
        <h3>Навігація</h3>
        <p>
          Перемикайте розділи за допомогою нижньої панелі.
          Щоб повернутися зі сторінки допомоги,
          натисніть «Назад» у верхній панелі.
        </p>
      </div>
    </div>

    <template #fixed>
      <AppTabbar active="about" />
    </template>
  </f7-page>
</template>

<script setup>
import AppTabbar from '../components/AppTabbar.vue';
</script>
