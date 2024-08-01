<!-- Fuente: https://tailwindcomponents.com/component/chat-layout -->
<template>
  <div class="bg-gray-100 h-screen flex flex-col max-w-lg mx-auto">
    <ChatHeader/>
    <ChatMessages />
    <MessageBox/>
  </div>
</template>
<script lang='ts' setup>
import { ref } from 'vue';
import ChatHeader from '../components/chat/ChatHeader.vue'
import ChatMessages from '../components/chat/ChatMessages.vue'
import MessageBox from '../components/chat/MessageBox.vue'

import type {ChatMessage} from '../interfaces/chat-message.interface'

const messages = ref<ChatMessage[]>([
  {
  id : new Date().getTime(),
  message : 'Hola mundo',
  itsMine : true
},
{
  id : new Date().getTime(),
  message : 'Hola je',
  itsMine : false,
  image : 'https://yesno.wtf/assets/no/7-331da2464250a1459cd7d41715e1f67d.gif'
},
])

</script>