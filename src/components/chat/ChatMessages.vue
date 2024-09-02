

<template>
  <div class="flex-1 overflow-y-auto p-4">
    <div class="flex flex-col space-y-2">
      <ChatBubble
        v-for="message in messages"
        :key="message.id"
        v-bind="message"
      />
      <!--
      <ChatBubble
        v-for="message in messages"
        :its-mine="message.itsMine"
        :key="message.id"
        :message="message.message"
        :image="message.image"
      />  
        -->
    </div>
  </div>
</template>

<style scoped></style>


<script setup lang="ts">
import ChatBubble from './ChatBubble.vue'

import { defineProps } from "vue"
import type { ChatMessage } from "../../interfaces/chat-message.interface"
interface Props{
  messages : ChatMessage[]
}

defineProps<Props>();
</script>