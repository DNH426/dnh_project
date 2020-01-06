<template>
    <v-app>
        <v-container>
            <v-col cols="12" md="12">
                <h1 class="headline mb-2 grey--text">Money Status</h1>
                <template>
                    <div id="app">
                        <GChart
                        type="ColumnChart"
                        :data="chartData"
                        :options="chartOptions"
                        />
                    </div>
                </template>
            </v-col>
        </v-container>
    </v-app>
</template>

<script>
export default {
    data: () => ({
        chartData:[
            ["Year", "Sales", "Expenses", "Profit"],
            ["2014", 1000, 2000, 3000],
            ["2015", 500, 750, 1000],
            ["2016", 100, 200, 300],
            ["2017", 2500, 3000, 1500],
        ],
        chartOptions:{
            chart:{
                title: "Company Performance",
                subtitle: "Sales, Expenses, and Profit: 2014-2017"
            }
        }
    }),

    name: 'App',
    components: {

    },
    computed: {
        theme(){
            return(this.$vuetify.theme.dark) ? 'dark' : 'light'
        }
    }
}
</script>

<style scoped>
</style>