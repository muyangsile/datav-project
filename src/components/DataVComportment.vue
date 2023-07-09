<template>
    <div class="bg">
        <dv-full-screen-container>

            <div class="module-box">
                <div style="flex: 0 1 25%;">
                    <dv-border-box-8 style="width: 100%; height: 150px;">

                        <dv-capsule-chart :config="config" style="width:100%;height:100%" />

                    </dv-border-box-8>
                </div>
                <div style="flex: 0 1 50%;">
                    <dv-border-box-8 style="width: 100%; height: 150px;">
                        <dv-digital-flop :config="config3" style="width:100%;height:100%" />
                    </dv-border-box-8>
                </div>
                <div style="flex: 0 1 25%;">
                    <dv-border-box-8 style="width: 100%; height: 150px;">dv-border-box-8</dv-border-box-8>
                </div>
            </div>

            <div class="module-box">
                <div style="flex: 0 1 25%;">
                    <dv-border-box-8 style="width: 100%; height: 600px;">dv-border-box-8</dv-border-box-8>
                </div>
                <div style="flex: 0 1 50%;">
                    <dv-border-box-8 style="width: 100%; height: 600px;">
                        
                       <Map/>
                    
                    </dv-border-box-8>
                </div>
                <div style="flex: 0 1 25%;">
                    <dv-border-box-8 style="width: 100%; height: 200px;">dv-border-box-8</dv-border-box-8>
                    <dv-border-box-8 style="width: 100%; height: 200px;">
                        <Chart/>
                    </dv-border-box-8>
                    <dv-border-box-8 style="width: 100%; height: 200px;">
                        <dv-water-level-pond :config="config2" style="width:100%;height:100%" />
                    </dv-border-box-8>
                </div>
            </div>

            <div class="module-box">
                <div style="flex: 0 1 100%;">
                    <dv-border-box-8 style="width: 100%; height: 200px;">dv-border-box-8</dv-border-box-8>
                </div>
            </div>


        </dv-full-screen-container>
    </div>
</template>
<script>

import Chart from './Chart.vue'
import Map from './Map.vue'

export default {
    components:{
        Chart,
        Map
    },
    data() {
        return {
            config: {
                data: [
                    {
                        name: '南阳',
                        value: 167
                    },
                    {
                        name: '周口',
                        value: 67
                    },
                    {
                        name: '漯河',
                        value: 123
                    },
                    {
                        name: '郑州',
                        value: 55
                    },
                    {
                        name: '西峡',
                        value: 98
                    }
                ]
            },
            config2: {
                data: [66, 45],
                shape: 'roundRect'
            },
            config3: {
                number: [100],
                toFixed: 2,
                content: '{nt}单'
            }
        }
    }

}
</script>
<style scoped>
.bg {
    color: #fff;
}

.module-box {
    display: flex;
}
</style>