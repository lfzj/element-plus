<template>
  <div class="demo-progress">
    <el-progress :percentage="50">
      <el-button type="text">Content</el-button>
    </el-progress>
    <el-progress
      :text-inside="true"
      :stroke-width="20"
      :percentage="50"
      status="exception"
    >
      <span>Content</span>
    </el-progress>
    <el-progress type="circle" :percentage="100" status="success">
      <el-button type="success" icon="el-icon-check" circle></el-button>
    </el-progress>
    <el-progress type="dashboard" :percentage="80">
      <template #default="{ percentage }">
        <span class="percentage-value">{{ percentage }}%</span>
        <span class="percentage-label">Progressing</span>
      </template>
    </el-progress>
  </div>
</template>

<style lang="scss" scoped>
.percentage-value {
  display: block;
  margin-top: 10px;
  font-size: 28px;
}

.percentage-label {
  display: block;
  margin-top: 10px;
  font-size: 12px;
}
</style>
