<template>
  <div id="transaction_list_box">
    <div id="transaction_list_wrap">
      <h3>Latest Transactions</h3>
      <a-divider />
      <ul size="small" bordered>
        <TransactionListItem v-for="item in data" :transaction="item" :key="item.txn" />
      </ul>
    </div>
  </div>
</template>
<script setup lang="ts">
import { ref, onMounted } from 'vue'
import { Transaction } from '~/types/transaction'
const data = ref<Array<Transaction>>([])

onMounted(() => {
  data.value = [{ txn: 'abdcefg' }]
})
</script>
<style scoped>
#transaction_list_box {
  display: flex;
  justify-content: center;
}
#transaction_list_wrap {
  width: calc(100% - 50px);
  margin-top: -30px;
  height: 300px;
  background-color: white;
  border-radius: 12px;

  h3 {
    padding: 15px 25px 0px 25px;
  }
}
</style>
../composables/transaction
