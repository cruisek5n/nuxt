<template>
  <section class="container">
    <a href="/">Top</a>
    <div>
      <h1>counter</h1>
      <p>count={{count}}</p>
      <button @click="addCount">カウントアップする</button>
    </div>
  </section>
</template>

<script lang="ts">
import { Component, Vue } from 'nuxt-property-decorator';

@Component
class Counter extends Vue {
  count: number = 0;
  addCount(): void {
    this.count++;
  }

  mounted(): void {
    console.log("ライフサイクルmounted");
  }
}

export default Counter;
</script>