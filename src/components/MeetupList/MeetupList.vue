<template>
  <v-container>
    <v-row>
      <Meetup
        v-for="meetup in filteredMeetups"
        :key="meetup._id"
        :meetup="meetup"
      />
    </v-row>
  </v-container>
</template>
<script>
import { mapGetters, mapActions } from 'vuex';
import Meetup from '@/components/Meetup/Meetup.vue';
export default {
  name: 'MeetupList',
  components: {
    Meetup,
  },
  computed: {
    ...mapGetters(['filteredMeetups']),
  },
  methods: {
    ...mapActions(['getAllMeetups']),
  },
  created() {
    this.getAllMeetups();
  },
};
</script>
