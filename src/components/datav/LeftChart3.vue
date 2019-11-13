<template>
  <div class="left-chart-3">
    <div class="lc3-header">桂林景点</div>
    <div class="lc3-details">游客总数<span>985684</span></div>
    <dv-capsule-chart class="lc3-chart" :config="config" />
  </div>
</template>

<script>
export default {
  name: 'LeftChart3',
  data () {
    return {
      config: {
        data: [
          {
            name: '两江四湖',
            value: 78234
          },
          {
            name: '十里画廊',
            value: 54532
          },
          {
            name: '龙脊梯田',
            value: 35233
          },
          {
            name: '漓江漂流',
            value: 46627
          },
          {
            name: '其他',
            value: 62312
          }
        ],
        colors: ['#00baff', '#3de7c9', '#fff', '#ffc530', '#469f4b']
      }
    }
  }
}
</script>

<style lang="less">
.left-chart-3 {
  width: 100%;
  height: 33%;
  display: flex;
  flex-direction: column;

  .lc3-header {
    height: 20px;
    line-height: 20px;
    font-size: 16px;
    text-indent: 20px;
    margin-top: 10px;
  }

  .lc3-details {
    height: 40px;
    font-size: 16px;
    display: flex;
    align-items: center;
    text-indent: 20px;

    span {
      color: #096dd9;
      font-weight: bold;
      font-size: 35px;
      margin-left: 20px;
    }
  }

  .lc3-chart {
    flex: 1;
  }
}
</style>
