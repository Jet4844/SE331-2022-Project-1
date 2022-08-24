<template>
  <!-- <router-link class="event-link"> -->
  <router-link
    class="event-link"
    :to="{ name: 'EventDetails', params: { id: people.id } }"
  >
    <div class="event-card">
      <h4>{{ people.name }} {{ people.surname }}</h4>
      <span>number of doses : {{ people.vaccine_status }}</span>
    </div>
  </router-link>
</template>

<script>
export default {
  name: 'EventCard',
  props: {
    people: {
      type: Object,
      required: true
    }
  }
}
</script>

<style scoped>
.event-card {
  padding: 20px;
  width: 250px;
  cursor: pointer;
  border: 1px solid #0a0a0a;
  margin-bottom: 18px;
  background-color: #a3fca2;
}
.event-card:hover {
  transform: scale(1.01);
  box-shadow: 0 3px 12px 0 rgba(0, 0, 0, 0.2);
}
.event-link {
  color: #0a0a0a;
  text-decoration: none;
}
</style>
