<template>
  <div class="football-news">
    <el-tabs type="border-card" class="demo-tabs">
      <el-tab-pane>
        <template #label>
          <span class="custom-tabs-label">
            <span>Nhận Định</span>
          </span>
        </template>
        <NewsList />
      </el-tab-pane>
      <el-tab-pane>
        <template #label>
          <span class="custom-tabs-label">
            <span>Soi Kèo</span>
          </span>
        </template>
        <NewsList />
      </el-tab-pane>
      <el-tab-pane>
        <template #label>
          <span class="custom-tabs-label">
            <span>Tỉ lệ</span>
          </span>
        </template>
        <NewsList />
      </el-tab-pane>
    </el-tabs>
  </div>
</template>

<script>
import NewsList from "./NewsList.vue";

export default {
  name: "FootballNews",
  components: {
    NewsList,
  },
};
</script>

<style lang="scss" scoped>
.football-news {
  padding: 0;
  margin: 16px 0;
  display: flex;
  flex-direction: column;
  height: calc(100dvh - 50px);
  background: white;
  min-width: 300px !important;

  .news-list {
    height: calc(100dvh - 106px);
  }

  .custom-tabs-label {
    display: flex;
    justify-content: center;
    align-items: center;
    height: 100%;
    font-size: 16px;
    font-weight: 500;
    margin: 16px 8px;
    white-space: nowrap;
    overflow: hidden;
  }

  .el-tabs__content {
    padding: 0 !important;
  }

  .el-tabs__item {
    .custom-tabs-label {
      background-color: #f5f5f5;
      color: #000;
      padding: 0 4px;
      margin-bottom: 8px;
      border-radius: 8px;
    }

    &.is-active {
      .custom-tabs-label {
        background-color: #ff004c;
        color: white;
      }
    }
  }
}
</style>
