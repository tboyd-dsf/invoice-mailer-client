<template>
  <v-data-table
    :headers="headers"
    :items="invoiceData"
    :items-per-page="5"
    class="elevation-1"
  ></v-data-table>
</template>

<script>
  export default {
    props: {
        invoiceData: {
            type: Array,
            required: true
        }
    },
    data () {
      return {
        headers: [
          {
            text: 'CG# (Invoice Number)',
            align: 'start',
            sortable: true,
            value: 'cg',
          },
          { text: 'Property', value: 'property' },
          { text: 'Email', value: 'email' }
        ],
      }
    },
  }
</script>

<style scoped>

</style>