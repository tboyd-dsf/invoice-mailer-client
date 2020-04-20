<template>
    <outgoing-invoices :invoiceData="invoiceData"></outgoing-invoices>
</template>

<script>
    import InvoiceData from '../db/testInvoiceData.json'
    import OutgoingInvoices from '../components/DashboardComps/OutgoingInvoices'
    export default {
        components: {
            OutgoingInvoices
        },
        data() {
            return {
                invoiceData: InvoiceData
            }
        }
    }
</script>

<style scoped>

</style>