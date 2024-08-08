<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Vue.js 3 + Chart.js + DataTables.js Example</title>
    <script src="https://cdn.jsdelivr.net/npm/vue@3"></script>
    <script src="https://cdn.jsdelivr.net/npm/chart.js"></script>
    <link rel="stylesheet" href="https://cdn.datatables.net/1.13.1/css/jquery.dataTables.min.css">
    <script src="https://code.jquery.com/jquery-3.5.1.js"></script>
    <script src="https://cdn.datatables.net/1.13.1/js/jquery.dataTables.min.js"></script>


    <link rel="stylesheet" type="text/css"
        href="https://cdnjs.cloudflare.com/ajax/libs/fomantic-ui/2.9.3/semantic.min.css">
    <script src="https://cdnjs.cloudflare.com/ajax/libs/fomantic-ui/2.9.3/semantic.min.js"></script>


    <style>
        #app {
            padding: 20px;
            color: #222831;
        }

        canvas {
            display: block;
            width: 100%;
            height: auto;
        }

        .row2 {
            display: flex;
            gap: 15px;
        }

        .row2 .card {
            width: 50%;
        }

        .row2 .ui.card {
            margin: 0;
        }

        #dashboardChart {
            max-width: 400px;
            height: 400px;
            display: block;
            margin: auto;
        }

        .dataTables_wrapper>.dataTables_length {
            margin-bottom: 20px;
        }

        .title {
            display: flex;
            justify-content: center;
            font-size: 24px;
            
           
            margin: 10px 0;
        }

        .title-wrapper {
            width: 70%;
            display: flex;
            background: linear-gradient(135deg, #ffafbd, #ffc3a0); /* Gradient background */
            padding: 20px;
            border-radius: 8px;
            color: #333;
            box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
            justify-content: space-between;
        }
        .title-wrapper p{
            font-size: 30px;
        }

        .doughnut p {
            display: flex;
            justify-content: center;
            font-size: 18px;
        }

        .block2 {
            display: flex;
            justify-content: center;
            align-items: center;
        }

        .info {
            margin-left: 30px;
            background-color: #faf3e0;
            border-radius: 8px;
            padding: 20px;
            box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
            max-width: 600px;

        }

        .text {
            margin: 10px 0;
            padding: 10px;
            border-radius: 6px;
            background: linear-gradient(135deg, #ffffe0, #ffffff);
            box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1);
        }   
        .right{
            display: flex;
           align-items: center;
        }
    </style>
</head>

<body>
    <div id="app">
        <div class="ui card" bis_skin_checked="1" style="width:100%">
            <div class="content" bis_skin_checked="1">
                <div class="header" bis_skin_checked="1">題目 1</div>
            </div>
            <div class="content" bis_skin_checked="1">
                <div v-if="error">
                    <p>Error: {{ error }}</p>
                </div>
                <table id="example" class="display ui celled table" style="width:100%">
                    <thead>
                        <tr>
                            <th>SID</th>
                            <th>INT_TEST</th>
                            <th>CHAR_TEST</th>
                            <th>DATE_TEST</th>
                            <th>TIME_TEST</th>
                        </tr>
                    </thead>
                    <tbody>

                    </tbody>
                </table>
            </div>
        </div>


        <div class="row2">
            <div class="ui card" bis_skin_checked="1">
                <div class="content" bis_skin_checked="1">
                    <div class="header" bis_skin_checked="1">題目 2</div>
                </div>
                <div class="content" bis_skin_checked="1">

                    <div class="chart-container">
                        <canvas id="myBarChart" width="500" height="200"></canvas>
                    </div>
                </div>
            </div>
            <div class="ui card" bis_skin_checked="1">
                <div class="content" bis_skin_checked="1">
                    <div class="header" bis_skin_checked="1">題目 3</div>
                </div>
                <div class="content" bis_skin_checked="1">
                    <div class="block">
                        <div class="ui slider" id="slider-1"></div>

                        <div class="ui right labeled input" bis_skin_checked="1">
                            <input v-model="oeeValue" type="text" placeholder="Enter weight.." disabled="">
                            <div class="ui basic label" bis_skin_checked="1">
                                %
                            </div>
                        </div>
                        <div class="title">
                            <div v-if="dataGrid2" class="title-wrapper">
                                {{ dataGrid2.Grid_Data[0].EQP_NO }}
                                <div class="right">
                                    {{ dataGrid2.Grid_Data[0].STATUS }}
                                    <i class="external alternate icon" style="visibility: visible; font-size: 24px;"></i>
                                </div>
                            </div>
                        </div>
                        <div class="block2">
                            <div class="doughnut">
                                <canvas id="dashboardChart"></canvas>
                                <div>
                                    <p><span>{{ oeeValue }}</span>%</p>
                                </div>
                            </div>
                            <div v-if="dataGrid2" class="info">
                                <div class="text"><p><strong>TOTAL_V:</strong> {{ dataGrid2.Grid_Data[0].TOTAL_V }}</p></div>
                                <div class="text"><p><strong>TOTAL_I:</strong> {{ dataGrid2.Grid_Data[0].TOTAL_I }}</p></div>
                                <div class="text"><p><strong>TOTAL_KW:</strong> {{ dataGrid2.Grid_Data[0].TOTAL_KW }}</p></div>
                                <div class="text"><p><strong>TOTAL_KWH:</strong> {{ dataGrid2.Grid_Data[0].TOTAL_KWH }}</p></div> 
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </div>



    </div>

    <script>
        const app = Vue.createApp({
            data() {
                return {
                    dataChart: null,
                    dataGrid: null,
                    dataGrid2: null,
                    error: null,
                    tokenKey: null,
                    oeeValue: 100,
                };
            },
            async created() {
                this.fetchChart();
                await this.fetchData('323017369146913');
                await this.fetchData('355596298610595');
            },
            mounted() {
                this.createDashboardChart();
                $('.ui.slider')
                    .slider({
                        min: 0,
                        max: 100,
                        start: this.oeeValue,
                        onChange: (value) => {
                            this.oeeValue = value;
                        }
                    });
            },
            watch: {
                oeeValue() {
                    this.updateDashboardChart();
                }
            },
            methods: {
                async fetchChart() {
                    try {
                        if (!this.tokenKey) {
                            await this.fetchTokenKey();
                        }

                        const response = await fetch('http://cloud.weyutech.com/API_TEST/api/GetChart', {
                            method: 'POST',
                            headers: {
                                'SID': '355597273880135',
                                'TokenKey': this.tokenKey
                            }
                        });

                        if (!response.ok) {
                            throw new Error('Network response was not ok ' + response.statusText);
                        }

                        this.dataChart = await response.json();
                        this.error = null;

                        this.initializeChart();

                    } catch (error) {
                        this.dataChart = null;
                        this.error = error.message;
                    }
                },


                async fetchData(sid) {
                    try {
                        if (!this.tokenKey) {
                            await this.fetchTokenKey();
                        }

                        const response = await fetch('http://cloud.weyutech.com/API_TEST/api/GetGrid', {
                            method: 'POST',
                            headers: {
                                'SID': sid,
                                'TokenKey': this.tokenKey
                            }
                        });

                        if (!response.ok) {
                            throw new Error('Network response was not ok ' + response.statusText);
                        }

                        const data = await response.json();

                        if (sid === '323017369146913') {
                            this.dataGrid = data;
                        } else if (sid === '355596298610595') {
                            this.dataGrid2 = data;
                        }

                        this.initializeDataTable();

                        this.error = null;
                    } catch (error) {
                        if (sid === '323017369146913') {
                            this.dataGrid = null;  // 清空第一個 SID 的資料
                        } else if (sid === '355596298610595') {
                            this.dataGrid2 = null;  // 清空第二個 SID 的資料
                        }
                        this.error = error.message;
                    }
                },

                async fetchTokenKey() {
                    try {
                        const response = await fetch('http://cloud.weyutech.com/API_TEST/api/WeyuLogin', {
                            method: 'POST',
                            headers: {
                                'Content-Type': 'application/json'
                            },
                            body: JSON.stringify({
                                UID: 'DEMO',
                                PWD: 'DEMO'
                            })
                        });

                        if (!response.ok) {
                            throw new Error('Network response was not ok ' + response.statusText);
                        }

                        const result = await response.json();
                        this.tokenKey = result.TokenKey;
                    } catch (error) {
                        this.error = error.message;
                    }
                },
                initializeChart() {
                    if (this.dataChart) {
                        var ctx = document.getElementById('myBarChart').getContext('2d');
                        new Chart(ctx, {
                            type: 'bar',
                            data: {
                                labels: this.dataChart.data.labels,
                                datasets: [{
                                    label: '用電量',
                                    backgroundColor: '#00ADB5',
                                    borderColor: '#EEEEEE',
                                    borderWidth: 1,
                                    maxBarThickness: 70,
                                    data: this.dataChart.data.datasets[0].data
                                }]
                            },
                            options: {
                                responsive: true,
                                scales: {
                                    x: {
                                        beginAtZero: true,
                                        title: {
                                            display: true,
                                            text: '年月份'
                                        }
                                    },
                                    y: {
                                        beginAtZero: true,
                                        title: {
                                            display: true,
                                            text: '用電量 (KWH)'
                                        }
                                    }
                                },
                                plugins: {
                                    legend: {
                                        display: true,
                                        position: 'top'
                                    },
                                    tooltip: {
                                        callbacks: {
                                            label: function (context) {
                                                return context.dataset.label + ': ' + context.raw.toLocaleString() + ' KWH';
                                            }
                                        }
                                    }
                                }
                            }
                        });
                    }
                },
                initializeDataTable() {
                    if ($.fn.DataTable.isDataTable('#example')) {
                        $('#example').DataTable().clear().destroy();
                    }

                    $('#example').DataTable({
                        data: this.dataGrid.Grid_Data || [],
                        columns: [
                            { data: 'SID' },
                            { data: 'INT_TEST' },
                            { data: 'CHAR_TEST' },
                            { data: 'DATE_TEST' },
                            { data: 'TIME_TEST' }
                        ]
                    });
                },
                createDashboardChart() {
                    const ctx = document.getElementById("dashboardChart").getContext("2d");
                    this.dashboardChart = new Chart(ctx, {
                        type: "doughnut",
                        data: {
                            labels: ['OEE'],
                            datasets: [{
                                label: 'OEE',
                                rotation: -90,
                                circumference: 180,
                                data: [this.oeeValue, 100 - this.oeeValue],
                                backgroundColor: [
                                    'rgba(32, 30, 67, 1)',
                                    'rgba(32, 30, 67, 0.2)',
                                ],
                                borderColor: [
                                    'rgba(255, 255, 255, 1)',
                                ],
                                hoverBackgroundColor: [
                                    'rgba(32, 30, 67, 1)',
                                    'rgba(32, 30, 67, 0.2)',
                                ],
                                hoverBorderColor: [
                                    'rgba(255, 255, 255, 1)',
                                ],
                                borderWidth: 5
                            }]
                        },
                        options: {
                            rotation: -90,
                            circumference: 180,
                            cutout: "90%",
                            plugins: {
                                title: {
                                    display: false,
                                    text: "Test01 Idle",
                                    color: '#333',
                                    font: {
                                        size: 20,
                                        weight: 'bold',
                                        family: 'Arial',
                                    },
                                    padding: {
                                        top: 20,
                                        bottom: 20
                                    },
                                    align: 'start',
                                    position: 'top'
                                },
                                legend: {
                                    display: false,
                                },
                                tooltip: {
                                    enabled: false,
                                    intersect: false,
                                }
                            },
                            interaction: {
                                intersect: false,
                                hover: false
                            }
                        }
                    });
                },
                updateDashboardChart() {
                    this.dashboardChart.data.datasets[0].data = [this.oeeValue, 100 - this.oeeValue];
                    this.dashboardChart.update();
                }
            }
        });

        app.mount('#app');
    </script>
</body>

</html>
