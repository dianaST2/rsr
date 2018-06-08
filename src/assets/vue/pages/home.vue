<template>
    <f7-page>
        <f7-navbar>
            <f7-nav-left>

                <f7-link class="panel-open" open-panel="left" icon="fa fa-bars"></f7-link>
            </f7-nav-left>
            <div class="title">This is personal desktop</div>
            <f7-nav-right>
                <f7-link class="searchbar-enable" data-searchbar=".searchbar-components" icon="fa fa-search"></f7-link>
            </f7-nav-right>
            <f7-searchbar class="searchbar-components" search-container=".components-list" search-in="a"
                          expandable></f7-searchbar>
        </f7-navbar>


        <!--<div class="card demo-facebook-card">-->
            <!--<div class="card-header">-->
                <!--<div class="demo-facebook-date">Friday at 9:30 AM</div>-->
            <!--</div>-->
        <!--</div>-->

        <div class="card-content card-content-padding">
            <div class="card-content card-content-padding">
                <img src="http://stroimsamolet.ru/wp-content/uploads/2017/08/passazhirskij-samolet_1.jpg" border=1 align="middle" width="100%"/>
                <!--<p class="text-align-center">Monday at 10.05 PM</p>-->
                <div class="card-content card-content-padding">
                </div>
            </div>
        </div>



        <div class="row">
            <div class="col-50">
                <div class="card">
                    <div class="col-50% button text-color-blue">1.Summary</div>
                    <div class="<div class=" card data-table>
                        <table>
                            <thead>
                            <tr>
                                <th class="label-cell">Наименование</th>
                                <th class="numeric-cell"></th>
                                <th class="numeric-cell">Заработная п</th>
                                <th class="numeric-cell">Время раб</th>
                                <th class="numeric-cell">Набор</th>
                            </tr>
                            </thead>
                            <tbody>
                            <tr>
                                <td class="label-cell">Pilot</td>
                                <td class="numeric-cell"></td>
                                <td class="numeric-cell">1500$</td>
                                <td class="numeric-cell">1.30</td>
                                <td class="numeric-cell">4</td>
                            </tr>
                            <tr>
                                <td class="label-cell">FA</td>
                                <td class="numeric-cell"></td>
                                <td class="numeric-cell">200$</td>
                                <td class="numeric-cell">1.30</td>
                                <td class="numeric-cell">0</td>
                            </tr>


                            </tbody>
                        </table>

                    </div>

                </div>

            </div>

            <div class="col-50">
                <div class="card">
                    <div class="ccol-50% button text-color-blue">2.Diagram</div>
                    <div class="card-content">

                    </div>

                </div>
            </div>
        </div>
        <div class="row">
            <div class="col-50">
                <div class="card">
                    <div class="col-50% button text-color-blue">3.Duty</div>
                    <div class="card-content">
                        <table>
                            <thead>
                            <tr>
                                <th class="label-cell">Наименование</th>
                                <th class="numeric-cell"></th>
                                <th class="numeric-cell">Бублики</th>
                                <th class="numeric-cell">Котлетки</th>
                                <th class="numeric-cell">Сосиски</th>
                            </tr>
                            </thead>
                            <tbody>
                            <tr>
                                <td class="label-cell">Импорт</td>
                                <td class="numeric-cell"></td>
                                <td class="numeric-cell">6</td>
                                <td class="numeric-cell">24</td>
                                <td class="numeric-cell">4</td>
                            </tr>
                            <tr>
                                <td class="label-cell">Экспорт</td>
                                <td class="numeric-cell">1</td>
                                <td class="numeric-cell">45</td>
                                <td class="numeric-cell">2</td>
                                <td class="numeric-cell">3</td>
                            </tr>
                            <tr>
                                <td class="label-cell">Экспорт</td>
                                <td class="numeric-cell">2</td>
                                <td class="numeric-cell">55</td>
                                <td class="numeric-cell">2</td>
                                <td class="numeric-cell">1</td>
                            </tr>
                            <tr>
                                <td class="label-cell">Экспорт</td>
                                <td class="numeric-cell">3</td>
                                <td class="numeric-cell">65</td>
                                <td class="numeric-cell">2</td>
                                <td class="numeric-cell">6</td>
                            </tr>


                            </tbody>
                        </table>
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
                        <table>
                            <thead>
                            <tr>
                                <th class="label-cell">Состояние</th>
                                <th class="numeric-cell">Рейс</th>
                                <th class="numeric-cell"></th>
                                <th class="numeric-cell">Авиакомпания</th>
                                <th class="numeric-cell">Статус</th>
                            </tr>
                            </thead>
                            <tbody>
                            <tr>
                                <td class="label-cell">Пож сигн</td>
                                <td class="numeric-cell">Y 261</td>
                                <td class="numeric-cell"></td>
                                <td class="numeric-cell">British Airways</td>
                                <td class="numeric-cell">Open</td>
                            </tr>
                            <tr>
                                <td class="label-cell">Самолёты</td>
                                <td class="numeric-cell">G 45</td>
                                <td class="numeric-cell"></td>
                                <td class="numeric-cell">Etihad</td>
                                <td class="numeric-cell">Problems</td>
                            </tr>


                            </tbody>
                        </table>
                    </div>

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
                        <div class="block block-strong text-align-center">
                            <div class="preloader color-green"></div>
                        </div>
                    </div>

                </div>
            </div>
        </div>


    </f7-page>
</template>
<script>

    export default {};

</script>
