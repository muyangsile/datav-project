<template>
    <div ref="chart" style="width: 100%;height:600px;"></div>
</template>
<script>
import * as echarts from 'echarts'
import chinaMap from '../assets/json/chian.json'
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
            echarts.registerMap('china', chinaMap);

            var option = {
                geo: {
                    show: true,
                    type: 'map',
                    map: 'china',
                    silent: true,
                    label: {
                        show: true, //文字显示
                        color: '#fff'
                    },
                    itemStyle: { //图形样式
                        areaColor: '#3353c7', //背景颜色
                        borderColor: '#fff', //边框颜色
                        borderWidth: 1 //边框粗细
                    },
                    zoom: 1.2 //放大倍数
                },
                series: [
                    {
                        type: 'effectScatter',   //  指明图表类型：带涟漪效果的散点图
                        coordinateSystem: 'geo', //  指明绘制在geo坐标系上
                        color: '#9fe080',   // 背景颜色
                        borderColor: 'rgb(255,0,0)',   // 边框颜色
                        symbolSize:20,
                        label: { //标签
                            normal: {
                                show: false
                            },
                            emphasis: {
                                show: false
                            }
                        },
                        itemStyle: {
                            normal: {
                                areaColor: "#0d0059",
                                borderColor: "#389dff",
                                borderWidth: 0.5
                            },
                            emphasis: {
                                areaColor: "#17008d",
                                shadowOffsetX: 0,
                                shadowOffsetY: 0,
                                shadowBlur: 5,
                                borderWidth: 0,
                                shadowColor: "rgba(0, 0, 0, 0.5)"
                            }
                        },
                        data: [
                            {
                                name: '上海',
                                value: [121.47, 31.23, 55]
                            },
                            {
                                name: '北京',
                                value: [116.40, 39.90, 110]
                            },
                            {
                                name: '重庆',
                                value: [106.55, 29.56, 32]    // value的前两项是经纬度坐标，第三项为污染度数据
                            }
                        ]
                    }
                ]
            };

            myChart.setOption(option);
        }
    }
}
</script>
<style></style>