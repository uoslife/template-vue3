<script setup lang="ts">
import styled from 'vue3-styled-components';

import Col from '@/components/layouts/Col.vue';

const TestElement = styled.div`
  background: ${props => props.theme.colors.Primary700};
`;
</script>

<template>
  <Col>
    <TestElement>Hello World!</TestElement>
  </Col>
</template>
