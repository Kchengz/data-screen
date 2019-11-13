<template>
  <div class="right-chart-1">
      <dv-scroll-board :config="config" />
  </div>
</template>

<script>
export default {
  name: 'RightChart1',
  data () {
    return {
      config: {
        header: ['城市', '游客量'],
        data: [
          ['南宁', '456456'],
          ['柳州', '128964'],
          ['桂林', '3456456'],
          ['梧州', '63445'],
          ['北海', '745678'],
          ['钦州', '735412'],
          ['玉林', '55278'],
          ['贵港', '62856'],
          ['防城港', '896125'],
          ['崇左', '892565'],
          ['来宾', '98965'],
          ['贺州', '18965'],
          ['河池', '38965'],
          ['百色', '687624']
        ],
        headerBGC: '#22ffff19',
        oddRowBGC: '#2299ff08',
        evenRowBGC: '#22ff6606',
        index: true,
        columnWidth: [50],
        align: ['center']
      }
    }
  }
}
</script>

<style lang="less">
.right-chart-1 {
  width: 100%;
  height: 100%;
  display: flex;
  flex-direction: column;

  .rc1-header {
    font-size: 24px;
    font-weight: bold;
    height: 30px;
    line-height: 30px;
  }

  .rc1-chart-container {
    flex: 1;
    display: flex;
  }

  .left {
    width: 30%;
    font-size: 16px;
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;

    .number {
      font-size: 34px;
      color: #096dd9;
      font-weight: bold;
      margin-bottom: 30px;
    }
  }

  .right {
    flex: 1;
    padding-bottom: 20px;
    padding-right: 20px;
    box-sizing: border-box;
  }
}
</style>
