<template>
  <div id="data-view">
    <dv-full-screen-container>
      <div class="main-header">
        <div class="mh-left">
          <!-- <dv-decoration-1 style="width:200px;height:50px;" /> -->
          <!-- 技术支持:<a href="https://github.com/jiaming743/DataV">https://github.com/jiaming743/DataV</a> -->
          </div>
        <div class="mh-middle">
          <!-- <dv-decoration-7 style="color:#7ec699;"> -->
            城市游客统计

          <!-- </dv-decoration-7> -->
          </div>
        <div class="mh-right">
          <dv-decoration-1 style="width:200px;height:50px;" />
          <!-- <dv-border-box-2
            style="width: 120px; height: 50px; line-height: 50px; text-align:center;margin-left:200px;"
          >
            综合管理台
          </dv-border-box-2> -->
        </div>
      </div>

      <div class="main-container">
        <dv-border-box-6 class="left-chart-container">

          <Left-Chart-1 />
          <Left-Chart-2 />
          <Left-Chart-3 />

        </dv-border-box-6>

        <div class="right-main-container">
          <div class="rmc-top-container">
            <dv-border-box-8 class="rmctc-left-container">

              <Center-Cmp />

            </dv-border-box-8>

            <div class="rmctc-right-container">
              <dv-border-box-5 class="rmctc-chart-1">

                <Right-Chart-1 />

              </dv-border-box-5>

              <dv-border-box-6 class="rmctc-chart-2">

                <Right-Chart-2 />

              </dv-border-box-6>
            </div>
          </div>

          <dv-border-box-6 class="rmc-bottom-container">

            <Bottom-Charts />

          </dv-border-box-6>
        </div>
      </div>

    </dv-full-screen-container>
  </div>
</template>

<script>
import LeftChart1 from './LeftChart1'
import LeftChart2 from './LeftChart2'
import LeftChart3 from './LeftChart3'

import CenterCmp from './CenterCmp'

import RightChart1 from './RightChart1'
import RightChart2 from './RightChart2'

import BottomCharts from './BottomCharts'

export default {
  name: 'DataView',
  components: {
    LeftChart1,
    LeftChart2,
    LeftChart3,
    CenterCmp,
    RightChart1,
    RightChart2,
    BottomCharts
  },
  data () {
    return {}
  }
}
</script>

<style lang="less">
#data-view {
  width: 100%;
  height: 100%;
  background-color: #030409;
  color: #fff;

  #dv-full-screen-container {
    background-image: url('./img/bg.png');
    background-size: 100% 100%;
    box-shadow: 0 0 3px blue;
    display: flex;
    flex-direction: column;
  }

  .main-header {
    height: 80px;
    display: flex;
    justify-content: space-between;
    align-items: flex-end;

    .mh-left {
      font-size: 20px;
      color: rgb(1,134,187);

      a:visited {
        color: rgb(1,134,187);
      }
    }

    .mh-middle {
      font-size: 30px;
      line-height:60px;
    }

    .mh-left, .mh-right {
      width: 450px;
    }
  }

  .main-container {
    height: calc(~"100% - 80px");
    display: flex;
    padding: 10px;
    box-sizing: border-box;

    .border-box-content {
      padding: 20px;
      box-sizing: border-box;
      display: flex;
    }
  }

  .left-chart-container {
    width: 22%;
    padding: 10px;
    box-sizing: border-box;

    .border-box-content {
      flex-direction: column;
    }
  }

  .right-main-container {
    width: 78%;
    padding-left: 5px;
    box-sizing: border-box;
  }

  .rmc-top-container {
    height: 65%;
    display: flex;
  }

  .rmctc-left-container {
    width: 50%;
  }

  .rmctc-right-container {
    width: 50%;
  }

  .rmc-bottom-container {
    height: 35%;
  }

  .rmctc-chart-1, .rmctc-chart-2 {
    height: 50%;
  }
}
</style>
