<template>
  <div v-if="GStore.event">
    <div id="nav">
      <router-link :to="{ name: 'EventDetails' }">Details</router-link>
      |
      <router-link :to="{ name: 'VaccineDetail' }">Vaccines</router-link> |
      <router-link :to="{ name: 'EventEdit' }">Comment</router-link>
    </div>
    <router-view :people="GStore.event" />
  </div>
</template>
<script>
export default {
  inject: ['GStore']
}
</script>
