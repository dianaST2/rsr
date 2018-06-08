<template>
    <f7-page>
        <f7-navbar>
            <f7-nav-left>

                <f7-link class="panel-open" open-panel="left" icon="fa fa-bars"></f7-link>
            </f7-nav-left>

            <H1>
                <div class="title">This is personal desktop</div>
            </H1>

            <f7-nav-right>
                <f7-link class="searchbar-enable" data-searchbar=".searchbar-components" icon="fa fa-search"></f7-link>
            </f7-nav-right>
            <f7-searchbar class="searchbar-components" search-container=".components-list" search-in="a"
                          expandable></f7-searchbar>
        </f7-navbar>



        <div class="card-content card-content-padding">
            <!--<div class="card-header">Monday at 10.05 PM </div>-->
            <div class="card-content card-content-padding">
                <div class="title-top">T</div>
                <img src="http://stroimsamolet.ru/wp-content/uploads/2017/08/passazhirskij-samolet_1.jpg" border=1 width="100%"/>
                <div class="card-content card-content-padding"></div></div></div>

        <div class="row">
            <div class="col-50">
                <div class="card">
                    <div class="col-50% button text-color-blue">1.Summary</div>

                    <div class="card data-table no-padding">
                        <table class="elevation-1">

                            <thead>
                            <tr>
                                <th class="label-cell">Время</th>
                                <th class="numeric-cell">Рейс</th>
                                <th class="numeric-cell">Направление</th>
                                <th class="numeric-cell">Авиакомпания</th>
                                <th class="numeric-cell">Статус</th>
                            </tr>
                            </thead>

                            <tr v-for="(result,index) in items">
                                <td class="text-xs-right">{{index}}</td>
                                <td>{{result.flight_number}}</td>
                                <td>{{result.ak}}</td>
                                <td>{{result.ap_1}}</td>
                                <td>{{result.ap_2}}</td>
                                <td>{{result.time_departure}}</td>
                                <td>{{result.check_in}}</td>
                                <td>{{result.gate}}</td>
                                <td>{{result.status}}</td>

                            </tr></table>
                    </div></div></div>

            <div class="col-50">
                <div class="card">
                    <div class="col-50% button text-color-blue">2.Diagram</div>
                    <div class="card-content">     <line-chart :chart-data="datacollection"></line-chart>

                    </div>
                    <div class="block block-strong text-align-center">
                        <div class=" preloader color-blue"></div></div>
                </div>
            </div>
        </div>
        <div class="row">
            <div class="col-50">
                <div class="card">
                    <div class="col-50% button text-color-blue">3.Duty</div>
                    <div class="card-content">

                    </div>

                </div>
            </div>
            <div class="col-50">
                <div class="card">
                    <div class="col-50% button text-color-blue">4.Flight map</div>
                    <div class="card-content">
                        <iframe src="https://www.google.com/maps/embed?pb=!1m16!1m12!1m3!1d16046.21698287076!2d30.290739200000004!3d59.81962239999999!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!4m1!3e6!5e0!3m2!1sru!2sru!4v1524821891393"
                                width="350" height="250" frameborder="0" style="border:0" allowfullscreen></iframe>


                    </div>

                </div>
            </div>

        </div>
        <div class="row">
            <div class="col-50">
                <div class="card">
                    <div class="col-50% button text-color-blue">5.Airport</div>
                    <div class="card-content">
                    </div>
                    <div class="block block-strong text-align-center">
                        <div class=" preloader color-pink"></div></div>

                </div>
            </div>
            <div class="col-50">
                <div class="card">
                    <div class="col-50% button text-color-blue">6.Status flight</div>
                    <div class="card-content">
                        <table>
                            <thead>
                            <tr>
                                <th class="label-cell">Время</th>
                                <th class="numeric-cell">Рейс</th>
                                <th class="numeric-cell">Направление</th>
                                <th class="numeric-cell">Авиакомпания</th>
                                <th class="numeric-cell">Статус</th>
                            </tr>
                            </thead>
                            <tbody>
                            <tr>
                                <td class="label-cell">00.05</td>
                                <td class="numeric-cell">Y 261</td>
                                <td class="numeric-cell">Oslo-New-York</td>
                                <td class="numeric-cell">British Airways</td>
                                <td class="numeric-cell">Open</td>
                            </tr>
                            <tr>
                                <td class="label-cell">00.10</td>
                                <td class="numeric-cell">G 45</td>
                                <td class="numeric-cell">Moscow-Dublin</td>
                                <td class="numeric-cell">Etihad</td>
                                <td class="numeric-cell">Open</td>
                            </tr>


                            </tbody>
                        </table>
                    </div>
                </div>
            </div>
            <div class="col-100">
                <div class="card">
                    <div class="col-100% button text-color-blue">7.Registration</div>
                    <div class="card-content">
                    </div>

                </div>
            </div>
        </div>


    </f7-page>
</template>
<script>
    import LineChart from './LineChart.js';

    export default {
        data(){
            return {
                items:[],
            datacollection: null
            }
        },
        components: {
            LineChart
        },
        methods: {
            getItems(){
                axios.get('http://rsr.loc/getFlights')
                    .then(response => {
                        this.items = response.data;
                    });
            },
            fillData () {
                this.datacollection = {
                    labels: [this.getRandomInt(), this.getRandomInt()],
                    datasets: [
                        {
                            label: 'Data One',
                            backgroundColor: '#4bf870',
                            data: [this.getRandomInt(), this.getRandomInt()]
                        }, {
                            label: 'Data One',
                            backgroundColor: '#71a3f8',
                            data: [this.getRandomInt(), this.getRandomInt()]
                        }
                    ]
                }
            },
            getRandomInt () {
                return Math.floor(Math.random() * (50 - 5 + 1)) + 5
            }
        },
        mounted(){
            this.fillData();
            this.getItems();
        }
    }

</script>

<style>
    .card-content{
        margin:40px 20px;
        box-sizing:border-box;
    }
    .title-top{
        display:block;
        text-align:center;
        margin:0 0 -58px 0;
        padding:10px 0;
        background:rgba(0,0,0,.6);
        color:white;
        opacity:.999;
    }
    .title-bottom{
        display:block;
        text-align:center;
        margin:-58px 0 0 0;
        padding:10px 0;
        background:rgba(0,0,0,.6);
        color:white;
        opacity:.999;
    }
    .card-content img{
        display:block;
        z-index:1;
        width:100%;
        margin:0 !important;
    }

    /*.blokbg1 {*/
        /*background-image: url("http://smexkartinka.ru/uploads/posts/2015-03/1427298296_23e6cef0.jpg");*/
        /*background-repeat: repeat;*/
        /*background-attachment: scroll;*/
    /*}*/

</style>