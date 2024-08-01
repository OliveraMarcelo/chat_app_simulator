<script setup lang="ts">
import ChatBubble from './ChatBubble.vue'
</script>

<template>
  <div class="flex-1 overflow-y-auto p-4">
    <div class="flex flex-col space-y-2">
      <ChatBubble :its-mine="true" message="Hola" />
      <ChatBubble
        :its-mine="false"
        message="no"
        image="https://yesno.wtf/assets/no/7-331da2464250a1459cd7d41715e1f67d.gif"
      />
    </div>
  </div>
</template>

<style scoped></style>
