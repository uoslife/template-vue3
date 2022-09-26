<script setup lang="ts">
import styled from 'vue3-styled-components';

const Layout = styled.div`
  background: ${({ theme }) => theme.colors.Secondary0};
  min-height: 100vh;
`;

const HeaderArea = styled.div``;

const ContentArea = styled.div`
  width: 1080px;
  margin: 0 auto;
`;

const FooterArea = styled.div``;
</script>

<template>
  <Layout>
    <HeaderArea>
      <slot name="header" />
    </HeaderArea>

    <ContentArea>
      <slot />
    </ContentArea>

    <FooterArea>
      <slot name="footer" />
    </FooterArea>
  </Layout>
</template>
