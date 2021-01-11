<template>
  <div>
    <TicketsList :tickets="tickets" />
  </div>
</template>

<script>
// @ is an alias to /src
import TicketsList from '@/components/Tickets/TicketsList.vue';

export default {
  name: 'Home',
  components: {
    TicketsList,
  },
  data(){
    return {
      tickets : [
        {
          id : 1,
          ticketNumber : 'n°1'
        }
      ]
    }
  }
}
</script>
