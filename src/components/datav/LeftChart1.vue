<template>
  <div class="left-chart-1">
    <div class="lc1-header">南宁景点</div>
    <div class="lc1-details">游客总数<span>868187</span></div>
    <dv-capsule-chart class="lc1-chart" :config="config" />
    <dv-decoration-4 :reverse="true" style="height:5px;" />
  </div>
</template>

<script>
export default {
  name: 'LeftChart1',
  data () {
    return {
      config: {
        data: [
          {
            name: '动物园',
            value: 21578
          },
          {
            name: '南湖公园',
            value: 11578
          },
          {
            name: '美丽南方',
            value: 20168
          },
          {
            name: '狮山公园',
            value: 12578
          },
          {
            name: '其他',
            value: 16354
          }
        ],
        colors: ['#00baff', '#3de7c9', '#fff', '#ffc530', '#469f4b']
        // unit: '人'
      }
    }
  }
}
</script>

<style lang="less">
.left-chart-1 {
  width: 100%;
  height: 37%;
  display: flex;
  flex-grow: 0;
  flex-direction: column;

  .lc1-header {
    text-align: center;
    height: 40px;
    display: flex;
    justify-content: center;
    align-items: center;
    font-size: 30px;
    margin-bottom: 20px;
  }

  .lc1-details {
    height: 50px;
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

  .lc1-chart {
    flex: 1;
  }
}
</style>
