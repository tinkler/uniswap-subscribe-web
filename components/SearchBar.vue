<template>
  <div class="scan-bar-wrap">
    <a-input-group class="search-input-group" compact>
      <a-select style="width: 130px;" v-model:value="filterSelect">
        <a-select-option value="">All</a-select-option>
        <a-select-option value="v2">Uniswap V2</a-select-option>
        <a-select-option value="v3">Uniswap V3</a-select-option>
      </a-select>
      <a-input-search
        v-model:value="filterPattern"
        placeholder="Search by Address / Txn Hash / Block / Token / Domain Name"
      ></a-input-search>
    </a-input-group>
    <div class="ad"></div>
  </div>
</template>
<script setup lang="ts">
import { ref } from 'vue'
const filterSelect = ref('')
const filterPattern = ref('')
</script>
<style scoped>
.scan-bar-wrap {
  background-color: rgba(8, 29, 53, 1);
  background-image: url(https://etherscan.io/images/svg/waves-light.svg);
  padding: 30px 10px 120px 10px;
  display: flex;
  .search-input-group {
    padding-left: 15px;
  }
}
.scan-bar-wrap .ad {
  width: 300px;
}
.ant-input-group.ant-input-group-compact {
  display: flex;
}
</style>
