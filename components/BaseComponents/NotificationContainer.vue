<template>
  <div class="flex flex-col-reverse fixed right-0 bottom-0 m-4" role="alert">
    <transition-group name="alert-slide">
      <Notification
        v-for="notification in notifications"
        :key="notification.id"
        class="mt-2"
        :notification="notification"
      />
    </transition-group>
  </div>
</template>

<script>
import { mapState } from 'vuex'

export default {
  name: 'NotificationContainer',
  computed: {
    ...mapState('notification', ['notifications']),
  },
}
</script>
