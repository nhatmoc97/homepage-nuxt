<template>
  <div class="trust-wrapper">
    <b-container>
      <p class="trust-title">{{ txt.TrustTitle }}</p>
      <div v-for="item in listTrustItems" :key="item.id" class="trust-list mt-3">
        <img :src="item.img" :alt="item.id" class="img-item">
      </div>
    </b-container>
  </div>
</template>

<script>
import { listTrustItems } from '@/static/shared/dummy'

export default {
  name: 'Trusted',
  data() {
    return {
      txt: {
        TrustTitle: 'Trusted by companies like'
      },
      listTrustItems: listTrustItems
    }
  }
}
</script>

<style lang="scss">
@use "static/base";

.trust-title {
  color: base.$primary-color;
  text-align: center;
}

.trust-wrapper {
  padding: 6rem 0;
}

.img-item {
  min-width: 5vh;
  margin: 0 2rem;
}

.trust-list {
  display: inline-flex;
  justify-content: center;
  align-items: center;
}
</style>
