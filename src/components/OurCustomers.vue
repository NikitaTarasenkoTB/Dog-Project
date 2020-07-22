<template>
  <MainPanel class="customers" :textPanelActive="true">
    <Title class="customers__title" :fontColor="'#5D62B5'">
      <template v-slot:title>
        Our CUSTOMERS
      </template>
      <template v-slot:subtitle>
        Illum qui dolorem eum quo voluptas ut distinctio
      </template>
    </Title>
  </MainPanel>
</template>

<script>
import MainPanel from '@/components/MainPanel';
import Title from '@/components/Title';
export default {
  components: {
    MainPanel,
    Title,
  }
}
</script>

<style scoped>

</style>