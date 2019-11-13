<template>
  <div class="center-cmp">
<dv-flyline-chart :config="config" style="width:100%;height:100%;" />
  </div>
</template>

<script>
import bgImgUrl from '@/assets/map.png'

export default {
  name: 'CenterCmp',
  data () {
    return {
      config: {
        centerPoint: [0.66, 0.70],
        points: [
          [0.62, 0.55],
          [0.68, 0.8],
          [0.72, 0.72],
          [0.5, 0.72],
          [0.72, 0.55],
          [0.68, 0.5],
          [0.8, 0.7],
          [0.5, 0.6],
          [0.5, 0.4],
          [0.42, 0.35],
          [0.48, 0.32],
          [0.3, 0.26],
          [0.2, 0.53],
          [0.18, 0.4],
          [0.16, 0.34],
          [0.8, 0.7],
          [0.8, 0.3]

        ],
        bgImgUrl
      }
    }
  }
}
</script>

<style lang="less">
.center-cmp {
  width: 100%;
  height: 100%;
  margin: 0px;
  padding: 0px;

}
</style>
