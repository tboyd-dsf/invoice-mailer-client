<template>
  <v-container>
    <v-row>
        <v-col cols="12">
            <outgoing-invoices :invoiceData="invoiceData"></outgoing-invoices>
        </v-col>
    </v-row>
    <v-row>
        <v-col cols="12">
            <customer-list :customerList="customerList"></customer-list>
        </v-col>
    </v-row>
    
  </v-container>
</template>

<script>
import InvoiceData from '../db/testInvoiceData.json'
import CustomerData from '../db/testCustomerListData.json'
import OutgoingInvoices from '../components/DashboardComps/OutgoingInvoices'
import CustomerList from '../components/DashboardComps/CustomerList'
export default {
  components: {
    OutgoingInvoices,
    CustomerList
  },
  data() {
    return {
      invoiceData: InvoiceData,
      customerList: CustomerData
    }
  }
}
</script>

<style scoped>
</style>