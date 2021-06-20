<template>
  <li>
    <span>{{ todoItem }}</span>
    <!-- 테스트 코드를 위해서 @click="$emit('remove')를 메소드 선언함"-->
    <button @click="removeItem">삭제</button>
  </li>
</template>

<script lang="ts">
import Vue from 'vue';

export default Vue.extend({
  props: {
    todoItem: String,
    index: Number,
  },
  methods: {
    removeItem() {
      this.$emit('remove', this.index);
    },
  },
});
</script>

<style scoped></style>
