<template>
  <f7-app v-bind="appParams">
    <f7-view main url="/" />
  </f7-app>
</template>

<script setup>
import routes from './routes.js';

const appParams = {
  name: 'TaskFlow',
  id: 'com.taskflow.app',
  theme: 'auto',
  routes,

  on: {
    pageBeforeOut(page) {
      const focusedElement = document.activeElement;

      if (
        focusedElement instanceof HTMLElement &&
        page.el.contains(focusedElement)
      ) {
        focusedElement.blur();
      }
    },

    pageAfterIn(page) {
      const heading = page.el.querySelector('.page-heading h1');

      if (heading instanceof HTMLElement) {
        heading.setAttribute('tabindex', '-1');
        heading.focus({ preventScroll: true });
      }
    },
  },
};
</script>