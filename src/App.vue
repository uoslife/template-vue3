<script setup lang="ts">
import { RouterView } from 'vue-router';
import { ThemeProvider } from 'vue3-styled-components';

import BaseLayout from '@/components/layouts/BaseLayout.vue';
import { DarkThemeColors, LightThemeColors } from '@/utils/styles';

const isDarkMode = window.matchMedia('(prefers-color-scheme: Dark)').matches;

const theme = {
  colors: isDarkMode ? DarkThemeColors : LightThemeColors,
};
</script>

<template>
  <ThemeProvider :theme="theme" :style="{ color: theme.colors.Secondary7 }">
    <BaseLayout>
      <RouterView />
    </BaseLayout>
  </ThemeProvider>
</template>
