<template>
  <FootballNews />
</template>

<script>
import FootballNews from "./components/News/index-news.vue";

export default {
  name: "App",
  components: {
    FootballNews,
  },
};
</script>

<style lang="scss">
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}

iframe#webpack-dev-server-client-overlay {
  display: none !important;
}

.el-tabs__header {
  margin: unset !important;
}

.el-tabs__content {
  height: inherit !important;
  overflow-y: overlay !important;

  &::webkit-scrollbar {
    width: 5px;
  }

  &::-webkit-scrollbar-track {
    background-color: #f0f0f0;
  }
}

@media only screen and (max-width: 768px) {
  .football-news {
    .news-list {
      height: unset !important;
    }
  }
}

.el-tabs__item {
  height: unset !important;
  padding: 0 !important;

  &.is-active {
    .matchup-schedule-daily-list-label {
      background-color: #f5d3cd !important;
      color: #f53f1f !important;

      span {
        color: #f53f1f !important;
      }
    }
  }
}

.el-tabs__nav-prev,
.el-tabs__nav-next {
  top: 50% !important;
  transform: translateY(-50%) !important;
}

.el-tabs--border-card {
  border: none !important;
}

.football-news {
  .el-tabs__header {
    background: white;
    margin-bottom: 16px !important;
    border: hidden !important;
    overflow: unset !important;
  }

  .el-tabs__nav-wrap {
    overflow: unset !important;
  }

  .el-tabs__nav-scroll {
    overflow: unset !important;
  }

  .el-tabs__content {
    padding: 0 !important;
  }

  .el-tabs__item {
    border: none !important;
  }

  .el-tabs {
    display: flex;
    flex-direction: column;
  }
}
</style>
