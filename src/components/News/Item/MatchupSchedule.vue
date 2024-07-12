<template>
  <div class="matchup-schedule">
    <div class="matchup-schedule-header">
      <h3>LỊCH BÓNG ĐÁ VIỆT NAM</h3>
      <a href="https://www.google.com.vn">Xem tất cả</a>
    </div>
    <div class="matchup-schedule-leage-select">
      <el-select v-model="selectedLeague" placeholder="Chọn giải đấu">
        <el-option
          v-for="league in leagues"
          :key="league.id"
          :label="league.name"
          :value="league.id"
        ></el-option>
      </el-select>
    </div>
    <el-tabs v-model="selectedDate" class="matchup-schedule-daily-list">
      <el-tab-pane
        v-for="(matchupList, date) in matchup"
        :key="date"
        :name="date"
        ><template #label>
          <div class="matchup-schedule-daily-list-label">
            <span>{{ getTabLabel(date) }}</span>
            <span>{{ formatDate(date) }}</span>
          </div>
        </template>
        <ul class="matchup-schedule-daily-list-item">
          <li v-for="matchup in matchupList" :key="matchup.matchup_time">
            <div class="home-info">
              <span>{{ matchup.home.team }}</span>
              <img src="../../../assets/manchester_united_PNG22.png" alt="" />
            </div>
            <div class="match-info">
              <div class="detail" v-if="[0, 1].includes(matchup.current_state)">
                <span>{{ matchup.home.score }} - {{ matchup.away.score }}</span>
                <span v-if="matchup.current_state == 1">
                  Hiệp {{ matchup.current_period }}:
                  {{ matchup.current_period_time }}'
                </span>
              </div>
              <span v-else-if="matchup.current_state === 2">
                <strong>{{ matchup.matchup_time }}</strong>
              </span>
            </div>
            <div class="away-info">
              <img src="../../../assets/manchester_united_PNG22.png" alt="" />
              <span>{{ matchup.away.team }}</span>
            </div>
          </li>
        </ul>
      </el-tab-pane>
    </el-tabs>
  </div>
</template>

<script>
import moment from "moment";
import { onMounted, ref } from "vue";

export default {
  props: {
    matchup: {
      type: Object,
      default: () => ({}),
    },
  },
  setup(props) {
    const selectedDate = ref("");

    const getTabLabel = (date) => {
      const today = moment().startOf("day");
      const givenDate = moment(date).startOf("day");

      if (today.isSame(givenDate)) {
        return "Today";
      }

      return moment(date).format("ddd");
    };

    const formatDate = (date) => {
      return moment(date).format("MM/DD");
    };

    const selectedLeague = ref("");
    const leagues = ref([
      {
        id: 1,
        name: "V-League",
      },
      {
        id: 2,
        name: "V-League 2",
      },
    ]);

    onMounted(() => {
      const today = moment().startOf("day").format("YYYY-MM-DD");
      if (today in props.matchup) {
        selectedDate.value = today;
      } else {
        selectedDate.value = Object.keys(props.matchup)[0] || "";
      }
    });

    return {
      formatDate,
      selectedDate,
      getTabLabel,
      selectedLeague,
      leagues,
    };
  },
};
</script>

<style lang="scss" scoped>
.matchup-schedule {
  min-width: 300px !important;
  margin: 16px;
  display: flex;
  flex-direction: column;
  border-radius: 8px;
  overflow: hidden;
  box-shadow: rgba(0, 0, 0, 0.02) 0px 1px 3px 0px,
    rgba(27, 31, 35, 0.15) 0px 0px 0px 1px;

  &-header {
    display: flex;
    justify-content: space-between;
    align-items: center;
    background: #18305e;
    color: white;
    padding: 0 16px;
    position: relative;

    &::before {
      content: "";
      position: absolute;
      top: 20%;
      left: 0;
      width: 5px;
      height: 60%;
      background: #f00;
    }

    h3 {
      margin-left: 16px;
      white-space: nowrap;
      overflow: ellipsis;
    }

    a {
      color: white;
      text-decoration: none;
      font-weight: 300;
      white-space: nowrap;
      overflow: hidden;

      &:hover {
        text-decoration: underline;
      }
    }
  }

  &-leage-select {
    padding: 12px;
    display: flex;

    .el-select {
      width: 200px;
    }
  }

  &-daily-list {
    background: #f0f0f0;
    height: calc(100dvh - 180px);

    &-label {
      display: flex;
      flex-direction: column;
      justify-content: space-between;
      align-items: center;
      padding: 8px;
      border-radius: 8px;
      margin: 10px;

      span {
        font-weight: 500;

        &:nth-child(1) {
          color: rgb(185, 185, 185);
        }
      }
    }

    &-item {
      list-style-type: none;
      padding: 0;
      margin: 6px 0;

      li {
        display: grid;
        grid-template-columns: 1fr 1fr 1fr;
        align-items: center;
        padding: 8px;
        background: white;
        border-radius: 8px;
        margin: 0 6px 6px 6px;
        height: 100%;
        overflow-y: auto;

        .home-info,
        .away-info {
          width: 100%;
          display: flex;
          flex-direction: row;
          align-items: center;
          justify-content: center;

          img {
            width: 32px;
            height: 32px;
          }

          span {
            margin: auto 10px;
          }
        }

        .match-info {
          display: flex;
          flex-direction: column;

          span {
            font-weight: 500;
            white-space: nowrap;
          }

          .detail {
            display: flex;
            flex-direction: column;

            span:nth-child(1) {
              font-weight: bold;
            }

            span:nth-child(2) {
              color: rgb(61, 199, 134);
            }
          }
        }
      }
    }
  }
}

@media only screen and (max-width: 768px) {
  .matchup-schedule {
    margin: 8px 0;
  }
}
</style>
