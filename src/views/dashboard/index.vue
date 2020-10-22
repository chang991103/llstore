<template>
  <div class="dashboard-container">
 <el-timeline>
    <el-timeline-item timestamp="2020/9/12" placement="top">
      <el-card>
        <h4>乐乐云商店</h4>
        <p>店员1 于 2020/9/12 20:46 上货 </p>
      </el-card>
    </el-timeline-item>
    <el-timeline-item timestamp="2020/9/15" placement="top">
      <el-card>
        <h4>乐乐云商店</h4>
        <p>店员2 于 2020/9/15 20:46 补货</p>
      </el-card>
    </el-timeline-item>
    <el-timeline-item timestamp="2018/4/2" placement="top">
      <el-card>
        <h4>乐乐云商店</h4>
        <p>店员3 于 2020/9/18 20:46 统计了店销售额</p>
      </el-card>
    </el-timeline-item>
  </el-timeline>
  <el-tag>月销售额差评百分比</el-tag>
<el-progress type="circle" :percentage="25"></el-progress>
  <el-tag>月销售额完成度百分比</el-tag>
<el-progress type="circle" :percentage="100" status="success"></el-progress>
  <el-tag>月员工积极度百分比</el-tag>
<el-progress type="circle" :percentage="70" status="warning"></el-progress>

  </div>
</template>

<script>
import { mapGetters } from 'vuex'

export default {
  name: 'Dashboard',
  computed: {
    ...mapGetters([
      'name'
    ])
  }
}
</script>

<style lang="scss" scoped>
 .is-selected {
    color: #1989FA;
  }
.dashboard {
  &-container {
    margin: 30px;
  }
  &-text {
    font-size: 30px;
    line-height: 46px;
  }
}
</style>
