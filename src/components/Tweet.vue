<script setup>
import User from '../components/User.vue';
import ProfileImage from '../components/ProfileImage.vue';
import Timestamp from '../components/Timestamp.vue';
import Message from '../components/Message.vue';
import Actions from '../components/Actions.vue';

const props = defineProps({
  user: Object,
  timestamp: String,
  message: String
});

</script>

<template>
  <div class="tweet">
    <ProfileImage image="user.image" />

    <div class="body">
      <div class="top">
        <User userData="user" />
        <Timestamp time="timestamp" />
      </div>

      <Message message="message" />
      <Actions />
    </div>

    <i class="fas fa-ellipsis-h"></i>
  </div>
</template>

<style scoped>
a {
  color: #42b983;
}
</style>
