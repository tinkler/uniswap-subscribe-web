<template>
  <li>{{ props.transaction.txn }}</li>
</template>

<script setup lang="ts">
  import { Transaction } from '~/types/transaction';
  const props = defineProps({
    transaction: {
      type: Object as () => Transaction,
      required: true,
    }
  })
</script>
<style scoped>
  li {
    list-style: none;
  }
</style>