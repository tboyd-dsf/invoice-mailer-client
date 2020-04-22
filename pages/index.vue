<template>
    <v-container>
        <v-row>
            <v-col cols="12" md="6" offset-md="3">
                <v-card>
                    <v-list-item>
                        <h1>Welcome to the Application</h1>
                    </v-list-item>
                    <v-list-item>
                        <p>Login to see Outgoing Invoices and Customer List</p>
                    </v-list-item>
                    <div class="my-12"></div>
                    <hr>
                    <v-card-actions>
                        <v-spacer></v-spacer>
                        <v-btn color="primary" to="/signup">
                            Login
                        </v-btn>
                    </v-card-actions>
                </v-card>
            </v-col>
        </v-row>
    </v-container>
</template>

<script>
    export default {
        
    }
</script>

<style scoped>

</style>