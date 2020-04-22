<template>
  <div>
    <h1>Customer List</h1>
    <v-data-table :headers="headers" :items="customerList" :items-per-page="5" class="elevation-1"></v-data-table>
  </div>
</template>

<script>
export default {
  props: {
    customerList: {
        type: Array,
        required: true
    }
  },
  data() {
    return {
      headers: [
        {
          text: 'Property',
          align: 'start',
          sortable: true,
          value: 'property'
        },
        { text: 'Email', value: 'email' },
        { text: 'Active', value: 'active' }
      ]
    }
  }
}
</script>

<style scoped>
</style>