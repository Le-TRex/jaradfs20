<template>
  <div>
    <TicketsList :tickets="tickets" />
  </div>
</template>

<script>
// @ is an alias to /src
import TicketsList from '@/components/Tickets/TicketsList.vue';
import ticketsService from '@/services/tickets';

export default {
  name: 'Home',
  components: {
    TicketsList,
  },
  data(){
    return {
      tickets : []
    }
  },
  async beforeCreate(){
    const tickets = await ticketsService.getTickets();
    //this.tickets ==> array vide du return
    //=tickets ==> les tickets obtenus grâce à getTickets()
    this.tickets = tickets;
  }
}
</script>
