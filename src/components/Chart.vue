<template>
    <div ref="chart" style="width: 100%;height:200px;"></div>
</template>
<script>

import * as echarts from 'echarts'

export default {
    data() {
        return {

        }
    },
    mounted() {
        this.initChart()
    },
    methods: {
        initChart() {
            var myChart = echarts.init(this.$refs.chart);
            // 绘制图表
            myChart.setOption({
               
                tooltip: {},
                xAxis: {
                    data: ['衬衫', '羊毛衫', '雪纺衫', '裤子', '高跟鞋', '袜子'],
                    axisLine:{
                        lineStyle:{
                            color:'#fff'
                        }
                    }
                },
                yAxis: {
                    axisLine:{
                        lineStyle:{
                            color:'#fff'
                        }
                    }
                },
                series: [
                    {
                        name: '销量',
                        type: 'bar',
                        data: [5, 20, 36, 10, 10, 20]
                    }
                ],
                grid:{
                    left:'10%',
                    right:'5%',
                    top:'10%',
                    bottom:'11%',
                    containLabel:false
                }
            });
        }
    }
}
</script>
<style></style>