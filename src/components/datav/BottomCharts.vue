<template>
  <div class="bottom-charts">
    <div class="bc-chart-item">
      <div class="bcci-header">南宁景点游客比例</div>
      <dv-active-ring-chart :config="config1" />
      <Label-Tag :config="labelConfig1" />
    </div>
<dv-decoration-4 style="width:5px;" />
    <div class="bc-chart-item">
      <div class="bcci-header">柳州景点游客比例</div>
      <dv-active-ring-chart :config="config2" />
      <Label-Tag :config="labelConfig2" />
    </div>

<dv-decoration-4 style="width:5px;" />
    <div class="bc-chart-item">
      <div class="bcci-header">桂林景点游客比例</div>
      <dv-active-ring-chart :config="config3" />
      <Label-Tag :config="labelConfig3" />
    </div>

    <!-- <dv-decoration-2 class="decoration-3" :reverse="true" style="width:5px;" />

    <div class="bc-chart-item">
      <div class="bcci-header">郑王收费站</div>
      <dv-active-ring-chart :config="config4" />
      <Label-Tag :config="labelConfig" />
    </div> -->

  </div>
</template>

<script>
import LabelTag from './LabelTag'

export default {
  name: 'BottomCharts',
  components: {
    LabelTag
  },
  data () {
    return {
      config1: {
        data: [
          {
            name: '动物园',
            value: 356
          },
          {
            name: '南湖公园',
            value: 215
          },
          {
            name: '美丽南方',
            value: 90
          },
          {
            name: '其他',
            value: 317
          }
        ],
        color: ['#00baff', '#3de7c9', '#fff', '#ffc530', '#469f4b'],
        radius: '65%',
        activeRadius: '70%'
      },
      labelConfig1: {
        data: ['动物园', '南湖公园', '美丽南方', '其他']
      },
      config2: {
        data: [
          {
            name: '百里柳江',
            value: 615
          },
          {
            name: '柳侯公园',
            value: 322
          },
          {
            name: '文庙',
            value: 198
          },
          {
            name: '其他',
            value: 80
          }
        ],
        color: ['#00baff', '#3de7c9', '#fff', '#ffc530', '#469f4b'],
        radius: '65%',
        activeRadius: '70%'
      },

      labelConfig2: {
        data: ['百里柳江', '柳侯公园', '文庙', '其他']
      },
      config3: {
        data: [
          {
            name: '两江四湖',
            value: 452
          },
          {
            name: '十里画廊',
            value: 512
          },
          {
            name: '龙脊梯田',
            value: 333
          },
          {
            name: '其他',
            value: 255
          }
        ],
        color: ['#00baff', '#3de7c9', '#fff', '#ffc530', '#469f4b'],
        radius: '65%',
        activeRadius: '70%'
      },

      labelConfig3: {
        data: ['两江四湖', '十里画廊', '龙脊梯田', '其他']
      }
    }
  }
}
</script>

<style lang="less">
.bottom-charts {
  width: 100%;
  height: 100%;
  display: flex;
  position: relative;

  .bc-chart-item {
    width: 33.33%;
    height: 100%;
    padding-top: 20px;
    box-sizing: border-box;
  }

  .bcci-header {
    height: 50px;
    text-align: center;
    line-height: 50px;
    font-size: 20px;
  }

  .dv-active-ring-chart {
    height: calc(~"100% - 80px");
  }

  .label-tag {
    height: 30px;
  }

  .active-ring-name {
    font-size: 18px !important;
  }

  .decoration-1, .decoration-2, .decoration-3 {
    display: absolute;
    left: 0%;
  }
}
</style>
