<template>
  <div class="right-chart-2">
<dv-scroll-ranking-board :config="config" />
  </div>
</template>

<script>
export default {
  name: 'RightChart2',
  data () {
    return {
      config: {
        data: [
          {
            name: '南宁',
            value: 551323
          },
          {
            name: '桂林',
            value: 541255
          },
          {
            name: '柳州',
            value: 323454
          },
          {
            name: '北海',
            value: 51224
          },
          {
            name: '防城港',
            value: 253551
          },
          {
            name: '来宾',
            value: 51352
          },
          {
            name: '梧州',
            value: 25129
          },
          {
            name: '贺州',
            value: 25129
          }
        ]
      }
    }
  }
}
</script>

<style lang="less">
.right-chart-2 {
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
