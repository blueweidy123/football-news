<template>
  <div class="container">
    <MatchupSchedule :matchup="matchupsList" />
    <FootballNews />
  </div>
</template>

<script>
import MatchupSchedule from "./Item/MatchupSchedule.vue";
import FootballNews from "./Item/FootballNews.vue";
import { ref } from "vue";

export default {
  components: {
    FootballNews,
    MatchupSchedule,
  },
  setup() {
    // Phân tích đề bài => api có thể là Get method với params là fromDate và toDate
    // => Em seed sẵn 1 object keyBy date
    const matchupsList = ref({
      "2024-07-11": [
        {
          matchup_time: "12:00",
          current_state: 0,
          current_period: 1,
          current_period_time: "60",
          home: {
            team: "Team A",
            score: 0,
            logo: "",
          },
          away: {
            team: "Team B",
            score: 0,
            logo: "",
          },
        },
        {
          matchup_time: "13:00",
          current_state: 0,
          current_period: 1,
          current_period_time: "60",
          home: {
            team: "Team C",
            score: 0,
            logo: "",
          },
          away: {
            team: "Team D",
            score: 0,
            logo: "",
          },
        },
        {
          matchup_time: "14:00",
          current_state: 1,
          current_period: 1,
          current_period_time: "60",
          home: {
            team: "Team E",
            score: 0,
            logo: "",
          },
          away: {
            team: "Team F",
            score: 0,
            logo: "",
          },
        },
        {
          matchup_time: "15:00",
          current_state: 1,
          current_period: 1,
          current_period_time: "60",
          home: {
            team: "Team G",
            score: 0,
            logo: "",
          },
          away: {
            team: "Team H",
            score: 0,
            logo: "",
          },
        },
        {
          matchup_time: "16:00",
          current_state: 2,
          current_period: 1,
          current_period_time: "60",
          home: {
            team: "Team I",
            score: 0,
            logo: "",
          },
          away: {
            team: "Team J",
            score: 0,
            logo: "",
          },
        },
        {
          matchup_time: "17:00",
          current_state: 2,
          current_period: 1,
          current_period_time: "60",
          home: {
            team: "Team K",
            score: 0,
            logo: "",
          },
          away: {
            team: "Team L",
            score: 0,
            logo: "",
          },
        },
        {
          matchup_time: "18:00",
          current_state: 2,
          current_period: 1,
          current_period_time: "60",
          home: {
            team: "Team M",
            score: 0,
            logo: "",
          },
          away: {
            team: "Team N",
            score: 0,
            logo: "",
          },
        },
        {
          matchup_time: "19:00",
          current_state: 2,
          current_period: 1,
          current_period_time: "60",
          home: {
            team: "Team O",
            score: 0,
            logo: "",
          },
          away: {
            team: "Team P",
            score: 0,
            logo: "",
          },
        },
        {
          matchup_time: "20:00",
          current_state: 2,
          current_period: 1,
          current_period_time: "60",
          home: {
            team: "Team Q",
            score: 0,
            logo: "",
          },
          away: {
            team: "Team R",
            score: 0,
            logo: "",
          },
        },
        {
          matchup_time: "21:00",
          current_state: 2,
          current_period: 1,
          current_period_time: "60",
          home: {
            team: "Team S",
            score: 0,
            logo: "",
          },
          away: {
            team: "Team T",
            score: 0,
            logo: "",
          },
        },
      ],
      "2024-07-12": [
        {
          matchup_time: "12:00",
          current_state: 0,
          current_period: 1,
          current_period_time: "60",
          home: {
            team: "Team A",
            score: 0,
            logo: "",
          },
          away: {
            team: "Team B",
            score: 0,
            logo: "",
          },
        },
        {
          matchup_time: "13:00",
          current_state: 0,
          current_period: 1,
          current_period_time: "60",
          home: {
            team: "Team C",
            score: 0,
            logo: "",
          },
          away: {
            team: "Team D",
            score: 0,
            logo: "",
          },
        },
        {
          matchup_time: "14:00",
          current_state: 1,
          current_period: 1,
          current_period_time: "60",
          home: {
            team: "Team E",
            score: 0,
            logo: "",
          },
          away: {
            team: "Team F",
            score: 0,
            logo: "",
          },
        },
        {
          matchup_time: "15:00",
          current_state: 1,
          current_period: 1,
          current_period_time: "60",
          home: {
            team: "Team G",
            score: 0,
            logo: "",
          },
          away: {
            team: "Team H",
            score: 0,
            logo: "",
          },
        },
        {
          matchup_time: "16:00",
          current_state: 2,
          current_period: 1,
          current_period_time: "60",
          home: {
            team: "Team I",
            score: 0,
            logo: "",
          },
          away: {
            team: "Team J",
            score: 0,
            logo: "",
          },
        },
        {
          matchup_time: "17:00",
          current_state: 2,
          current_period: 1,
          current_period_time: "60",
          home: {
            team: "Team K",
            score: 0,
            logo: "",
          },
          away: {
            team: "Team L",
            score: 0,
            logo: "",
          },
        },
        {
          matchup_time: "18:00",
          current_state: 2,
          current_period: 1,
          current_period_time: "60",
          home: {
            team: "Team M",
            score: 0,
            logo: "",
          },
          away: {
            team: "Team N",
            score: 0,
            logo: "",
          },
        },
        {
          matchup_time: "19:00",
          current_state: 2,
          current_period: 1,
          current_period_time: "60",
          home: {
            team: "Team O",
            score: 0,
            logo: "",
          },
          away: {
            team: "Team P",
            score: 0,
            logo: "",
          },
        },
        {
          matchup_time: "20:00",
          current_state: 2,
          current_period: 1,
          current_period_time: "60",
          home: {
            team: "Team Q",
            score: 0,
            logo: "",
          },
          away: {
            team: "Team R",
            score: 0,
            logo: "",
          },
        },
        {
          matchup_time: "21:00",
          current_state: 2,
          current_period: 1,
          current_period_time: "60",
          home: {
            team: "Team S",
            score: 0,
            logo: "",
          },
          away: {
            team: "Team T",
            score: 0,
            logo: "",
          },
        },
      ],
      "2024-07-13": [
        {
          matchup_time: "12:00",
          current_state: 0,
          current_period: 1,
          current_period_time: "60",
          home: {
            team: "Team A",
            score: 0,
            logo: "",
          },
          away: {
            team: "Team B",
            score: 0,
            logo: "",
          },
        },
        {
          matchup_time: "13:00",
          current_state: 0,
          current_period: 1,
          current_period_time: "60",
          home: {
            team: "Team C",
            score: 0,
            logo: "",
          },
          away: {
            team: "Team D",
            score: 0,
            logo: "",
          },
        },
        {
          matchup_time: "14:00",
          current_state: 1,
          current_period: 1,
          current_period_time: "60",
          home: {
            team: "Team E",
            score: 0,
            logo: "",
          },
          away: {
            team: "Team F",
            score: 0,
            logo: "",
          },
        },
        {
          matchup_time: "15:00",
          current_state: 1,
          current_period: 1,
          current_period_time: "60",
          home: {
            team: "Team G",
            score: 0,
            logo: "",
          },
          away: {
            team: "Team H",
            score: 0,
            logo: "",
          },
        },
        {
          matchup_time: "16:00",
          current_state: 2,
          current_period: 1,
          current_period_time: "60",
          home: {
            team: "Team I",
            score: 0,
            logo: "",
          },
          away: {
            team: "Team J",
            score: 0,
            logo: "",
          },
        },
        {
          matchup_time: "17:00",
          current_state: 2,
          current_period: 1,
          current_period_time: "60",
          home: {
            team: "Team K",
            score: 0,
            logo: "",
          },
          away: {
            team: "Team L",
            score: 0,
            logo: "",
          },
        },
        {
          matchup_time: "18:00",
          current_state: 2,
          current_period: 1,
          current_period_time: "60",
          home: {
            team: "Team M",
            score: 0,
            logo: "",
          },
          away: {
            team: "Team N",
            score: 0,
            logo: "",
          },
        },
        {
          matchup_time: "19:00",
          current_state: 2,
          current_period: 1,
          current_period_time: "60",
          home: {
            team: "Team O",
            score: 0,
            logo: "",
          },
          away: {
            team: "Team P",
            score: 0,
            logo: "",
          },
        },
        {
          matchup_time: "20:00",
          current_state: 2,
          current_period: 1,
          current_period_time: "60",
          home: {
            team: "Team Q",
            score: 0,
            logo: "",
          },
          away: {
            team: "Team R",
            score: 0,
            logo: "",
          },
        },
        {
          matchup_time: "21:00",
          current_state: 2,
          current_period: 1,
          current_period_time: "60",
          home: {
            team: "Team S",
            score: 0,
            logo: "",
          },
          away: {
            team: "Team T",
            score: 0,
            logo: "",
          },
        },
      ],
      "2024-07-14": [
        {
          matchup_time: "12:00",
          current_state: 0,
          current_period: 1,
          current_period_time: "60",
          home: {
            team: "Team A",
            score: 0,
            logo: "",
          },
          away: {
            team: "Team B",
            score: 0,
            logo: "",
          },
        },
        {
          matchup_time: "13:00",
          current_state: 0,
          current_period: 1,
          current_period_time: "60",
          home: {
            team: "Team C",
            score: 0,
            logo: "",
          },
          away: {
            team: "Team D",
            score: 0,
            logo: "",
          },
        },
        {
          matchup_time: "14:00",
          current_state: 1,
          current_period: 1,
          current_period_time: "60",
          home: {
            team: "Team E",
            score: 0,
            logo: "",
          },
          away: {
            team: "Team F",
            score: 0,
            logo: "",
          },
        },
        {
          matchup_time: "15:00",
          current_state: 1,
          current_period: 1,
          current_period_time: "60",
          home: {
            team: "Team G",
            score: 0,
            logo: "",
          },
          away: {
            team: "Team H",
            score: 0,
            logo: "",
          },
        },
        {
          matchup_time: "16:00",
          current_state: 2,
          current_period: 1,
          current_period_time: "60",
          home: {
            team: "Team I",
            score: 0,
            logo: "",
          },
          away: {
            team: "Team J",
            score: 0,
            logo: "",
          },
        },
        {
          matchup_time: "17:00",
          current_state: 2,
          current_period: 1,
          current_period_time: "60",
          home: {
            team: "Team K",
            score: 0,
            logo: "",
          },
          away: {
            team: "Team L",
            score: 0,
            logo: "",
          },
        },
        {
          matchup_time: "18:00",
          current_state: 2,
          current_period: 1,
          current_period_time: "60",
          home: {
            team: "Team M",
            score: 0,
            logo: "",
          },
          away: {
            team: "Team N",
            score: 0,
            logo: "",
          },
        },
        {
          matchup_time: "19:00",
          current_state: 2,
          current_period: 1,
          current_period_time: "60",
          home: {
            team: "Team O",
            score: 0,
            logo: "",
          },
          away: {
            team: "Team P",
            score: 0,
            logo: "",
          },
        },
        {
          matchup_time: "20:00",
          current_state: 2,
          current_period: 1,
          current_period_time: "60",
          home: {
            team: "Team Q",
            score: 0,
            logo: "",
          },
          away: {
            team: "Team R",
            score: 0,
            logo: "",
          },
        },
        {
          matchup_time: "21:00",
          current_state: 2,
          current_period: 1,
          current_period_time: "60",
          home: {
            team: "Team S",
            score: 0,
            logo: "",
          },
          away: {
            team: "Team T",
            score: 0,
            logo: "",
          },
        },
      ],
      "2024-07-15": [
        {
          matchup_time: "12:00",
          current_state: 0,
          current_period: 1,
          current_period_time: "60",
          home: {
            team: "Team A",
            score: 0,
            logo: "",
          },
          away: {
            team: "Team B",
            score: 0,
            logo: "",
          },
        },
        {
          matchup_time: "13:00",
          current_state: 0,
          current_period: 1,
          current_period_time: "60",
          home: {
            team: "Team C",
            score: 0,
            logo: "",
          },
          away: {
            team: "Team D",
            score: 0,
            logo: "",
          },
        },
        {
          matchup_time: "14:00",
          current_state: 1,
          current_period: 1,
          current_period_time: "60",
          home: {
            team: "Team E",
            score: 0,
            logo: "",
          },
          away: {
            team: "Team F",
            score: 0,
            logo: "",
          },
        },
        {
          matchup_time: "15:00",
          current_state: 1,
          current_period: 1,
          current_period_time: "60",
          home: {
            team: "Team G",
            score: 0,
            logo: "",
          },
          away: {
            team: "Team H",
            score: 0,
            logo: "",
          },
        },
        {
          matchup_time: "16:00",
          current_state: 2,
          current_period: 1,
          current_period_time: "60",
          home: {
            team: "Team I",
            score: 0,
            logo: "",
          },
          away: {
            team: "Team J",
            score: 0,
            logo: "",
          },
        },
        {
          matchup_time: "17:00",
          current_state: 2,
          current_period: 1,
          current_period_time: "60",
          home: {
            team: "Team K",
            score: 0,
            logo: "",
          },
          away: {
            team: "Team L",
            score: 0,
            logo: "",
          },
        },
        {
          matchup_time: "18:00",
          current_state: 2,
          current_period: 1,
          current_period_time: "60",
          home: {
            team: "Team M",
            score: 0,
            logo: "",
          },
          away: {
            team: "Team N",
            score: 0,
            logo: "",
          },
        },
        {
          matchup_time: "19:00",
          current_state: 2,
          current_period: 1,
          current_period_time: "60",
          home: {
            team: "Team O",
            score: 0,
            logo: "",
          },
          away: {
            team: "Team P",
            score: 0,
            logo: "",
          },
        },
        {
          matchup_time: "20:00",
          current_state: 2,
          current_period: 1,
          current_period_time: "60",
          home: {
            team: "Team Q",
            score: 0,
            logo: "",
          },
          away: {
            team: "Team R",
            score: 0,
            logo: "",
          },
        },
        {
          matchup_time: "21:00",
          current_state: 2,
          current_period: 1,
          current_period_time: "60",
          home: {
            team: "Team S",
            score: 0,
            logo: "",
          },
          away: {
            team: "Team T",
            score: 0,
            logo: "",
          },
        },
      ],
      "2024-07-16": [
        {
          matchup_time: "12:00",
          current_state: 0,
          current_period: 1,
          current_period_time: "60",
          home: {
            team: "Team A",
            score: 0,
            logo: "",
          },
          away: {
            team: "Team B",
            score: 0,
            logo: "",
          },
        },
        {
          matchup_time: "13:00",
          current_state: 0,
          current_period: 1,
          current_period_time: "60",
          home: {
            team: "Team C",
            score: 0,
            logo: "",
          },
          away: {
            team: "Team D",
            score: 0,
            logo: "",
          },
        },
        {
          matchup_time: "14:00",
          current_state: 1,
          current_period: 1,
          current_period_time: "60",
          home: {
            team: "Team E",
            score: 0,
            logo: "",
          },
          away: {
            team: "Team F",
            score: 0,
            logo: "",
          },
        },
        {
          matchup_time: "15:00",
          current_state: 1,
          current_period: 1,
          current_period_time: "60",
          home: {
            team: "Team G",
            score: 0,
            logo: "",
          },
          away: {
            team: "Team H",
            score: 0,
            logo: "",
          },
        },
        {
          matchup_time: "16:00",
          current_state: 2,
          current_period: 1,
          current_period_time: "60",
          home: {
            team: "Team I",
            score: 0,
            logo: "",
          },
          away: {
            team: "Team J",
            score: 0,
            logo: "",
          },
        },
        {
          matchup_time: "17:00",
          current_state: 2,
          current_period: 1,
          current_period_time: "60",
          home: {
            team: "Team K",
            score: 0,
            logo: "",
          },
          away: {
            team: "Team L",
            score: 0,
            logo: "",
          },
        },
        {
          matchup_time: "18:00",
          current_state: 2,
          current_period: 1,
          current_period_time: "60",
          home: {
            team: "Team M",
            score: 0,
            logo: "",
          },
          away: {
            team: "Team N",
            score: 0,
            logo: "",
          },
        },
        {
          matchup_time: "19:00",
          current_state: 2,
          current_period: 1,
          current_period_time: "60",
          home: {
            team: "Team O",
            score: 0,
            logo: "",
          },
          away: {
            team: "Team P",
            score: 0,
            logo: "",
          },
        },
        {
          matchup_time: "20:00",
          current_state: 2,
          current_period: 1,
          current_period_time: "60",
          home: {
            team: "Team Q",
            score: 0,
            logo: "",
          },
          away: {
            team: "Team R",
            score: 0,
            logo: "",
          },
        },
        {
          matchup_time: "21:00",
          current_state: 2,
          current_period: 1,
          current_period_time: "60",
          home: {
            team: "Team S",
            score: 0,
            logo: "",
          },
          away: {
            team: "Team T",
            score: 0,
            logo: "",
          },
        },
      ],
      "2024-07-17": [
        {
          matchup_time: "12:00",
          current_state: 0,
          current_period: 1,
          current_period_time: "60",
          home: {
            team: "Team A",
            score: 0,
            logo: "",
          },
          away: {
            team: "Team B",
            score: 0,
            logo: "",
          },
        },
        {
          matchup_time: "13:00",
          current_state: 0,
          current_period: 1,
          current_period_time: "60",
          home: {
            team: "Team C",
            score: 0,
            logo: "",
          },
          away: {
            team: "Team D",
            score: 0,
            logo: "",
          },
        },
        {
          matchup_time: "14:00",
          current_state: 1,
          current_period: 1,
          current_period_time: "60",
          home: {
            team: "Team E",
            score: 0,
            logo: "",
          },
          away: {
            team: "Team F",
            score: 0,
            logo: "",
          },
        },
        {
          matchup_time: "15:00",
          current_state: 1,
          current_period: 1,
          current_period_time: "60",
          home: {
            team: "Team G",
            score: 0,
            logo: "",
          },
          away: {
            team: "Team H",
            score: 0,
            logo: "",
          },
        },
        {
          matchup_time: "16:00",
          current_state: 2,
          current_period: 1,
          current_period_time: "60",
          home: {
            team: "Team I",
            score: 0,
            logo: "",
          },
          away: {
            team: "Team J",
            score: 0,
            logo: "",
          },
        },
        {
          matchup_time: "17:00",
          current_state: 2,
          current_period: 1,
          current_period_time: "60",
          home: {
            team: "Team K",
            score: 0,
            logo: "",
          },
          away: {
            team: "Team L",
            score: 0,
            logo: "",
          },
        },
        {
          matchup_time: "18:00",
          current_state: 2,
          current_period: 1,
          current_period_time: "60",
          home: {
            team: "Team M",
            score: 0,
            logo: "",
          },
          away: {
            team: "Team N",
            score: 0,
            logo: "",
          },
        },
        {
          matchup_time: "19:00",
          current_state: 2,
          current_period: 1,
          current_period_time: "60",
          home: {
            team: "Team O",
            score: 0,
            logo: "",
          },
          away: {
            team: "Team P",
            score: 0,
            logo: "",
          },
        },
        {
          matchup_time: "20:00",
          current_state: 2,
          current_period: 1,
          current_period_time: "60",
          home: {
            team: "Team Q",
            score: 0,
            logo: "",
          },
          away: {
            team: "Team R",
            score: 0,
            logo: "",
          },
        },
        {
          matchup_time: "21:00",
          current_state: 2,
          current_period: 1,
          current_period_time: "60",
          home: {
            team: "Team S",
            score: 0,
            logo: "",
          },
          away: {
            team: "Team T",
            score: 0,
            logo: "",
          },
        },
      ],
      "2024-07-18": [
        {
          matchup_time: "12:00",
          current_state: 0,
          current_period: 1,
          current_period_time: "60",
          home: {
            team: "Team A",
            score: 0,
            logo: "",
          },
          away: {
            team: "Team B",
            score: 0,
            logo: "",
          },
        },
        {
          matchup_time: "13:00",
          current_state: 0,
          current_period: 1,
          current_period_time: "60",
          home: {
            team: "Team C",
            score: 0,
            logo: "",
          },
          away: {
            team: "Team D",
            score: 0,
            logo: "",
          },
        },
        {
          matchup_time: "14:00",
          current_state: 1,
          current_period: 1,
          current_period_time: "60",
          home: {
            team: "Team E",
            score: 0,
            logo: "",
          },
          away: {
            team: "Team F",
            score: 0,
            logo: "",
          },
        },
        {
          matchup_time: "15:00",
          current_state: 1,
          current_period: 1,
          current_period_time: "60",
          home: {
            team: "Team G",
            score: 0,
            logo: "",
          },
          away: {
            team: "Team H",
            score: 0,
            logo: "",
          },
        },
        {
          matchup_time: "16:00",
          current_state: 2,
          current_period: 1,
          current_period_time: "60",
          home: {
            team: "Team I",
            score: 0,
            logo: "",
          },
          away: {
            team: "Team J",
            score: 0,
            logo: "",
          },
        },
        {
          matchup_time: "17:00",
          current_state: 2,
          current_period: 1,
          current_period_time: "60",
          home: {
            team: "Team K",
            score: 0,
            logo: "",
          },
          away: {
            team: "Team L",
            score: 0,
            logo: "",
          },
        },
        {
          matchup_time: "18:00",
          current_state: 2,
          current_period: 1,
          current_period_time: "60",
          home: {
            team: "Team M",
            score: 0,
            logo: "",
          },
          away: {
            team: "Team N",
            score: 0,
            logo: "",
          },
        },
        {
          matchup_time: "19:00",
          current_state: 2,
          current_period: 1,
          current_period_time: "60",
          home: {
            team: "Team O",
            score: 0,
            logo: "",
          },
          away: {
            team: "Team P",
            score: 0,
            logo: "",
          },
        },
        {
          matchup_time: "20:00",
          current_state: 2,
          current_period: 1,
          current_period_time: "60",
          home: {
            team: "Team Q",
            score: 0,
            logo: "",
          },
          away: {
            team: "Team R",
            score: 0,
            logo: "",
          },
        },
        {
          matchup_time: "21:00",
          current_state: 2,
          current_period: 1,
          current_period_time: "60",
          home: {
            team: "Team S",
            score: 0,
            logo: "",
          },
          away: {
            team: "Team T",
            score: 0,
            logo: "",
          },
        },
      ],
      "2024-07-19": [
        {
          matchup_time: "12:00",
          current_state: 0,
          current_period: 1,
          current_period_time: "60",
          home: {
            team: "Team A",
            score: 0,
            logo: "",
          },
          away: {
            team: "Team B",
            score: 0,
            logo: "",
          },
        },
        {
          matchup_time: "13:00",
          current_state: 0,
          current_period: 1,
          current_period_time: "60",
          home: {
            team: "Team C",
            score: 0,
            logo: "",
          },
          away: {
            team: "Team D",
            score: 0,
            logo: "",
          },
        },
        {
          matchup_time: "14:00",
          current_state: 1,
          current_period: 1,
          current_period_time: "60",
          home: {
            team: "Team E",
            score: 0,
            logo: "",
          },
          away: {
            team: "Team F",
            score: 0,
            logo: "",
          },
        },
        {
          matchup_time: "15:00",
          current_state: 1,
          current_period: 1,
          current_period_time: "60",
          home: {
            team: "Team G",
            score: 0,
            logo: "",
          },
          away: {
            team: "Team H",
            score: 0,
            logo: "",
          },
        },
        {
          matchup_time: "16:00",
          current_state: 2,
          current_period: 1,
          current_period_time: "60",
          home: {
            team: "Team I",
            score: 0,
            logo: "",
          },
          away: {
            team: "Team J",
            score: 0,
            logo: "",
          },
        },
        {
          matchup_time: "17:00",
          current_state: 2,
          current_period: 1,
          current_period_time: "60",
          home: {
            team: "Team K",
            score: 0,
            logo: "",
          },
          away: {
            team: "Team L",
            score: 0,
            logo: "",
          },
        },
        {
          matchup_time: "18:00",
          current_state: 2,
          current_period: 1,
          current_period_time: "60",
          home: {
            team: "Team M",
            score: 0,
            logo: "",
          },
          away: {
            team: "Team N",
            score: 0,
            logo: "",
          },
        },
        {
          matchup_time: "19:00",
          current_state: 2,
          current_period: 1,
          current_period_time: "60",
          home: {
            team: "Team O",
            score: 0,
            logo: "",
          },
          away: {
            team: "Team P",
            score: 0,
            logo: "",
          },
        },
        {
          matchup_time: "20:00",
          current_state: 2,
          current_period: 1,
          current_period_time: "60",
          home: {
            team: "Team Q",
            score: 0,
            logo: "",
          },
          away: {
            team: "Team R",
            score: 0,
            logo: "",
          },
        },
        {
          matchup_time: "21:00",
          current_state: 2,
          current_period: 1,
          current_period_time: "60",
          home: {
            team: "Team S",
            score: 0,
            logo: "",
          },
          away: {
            team: "Team T",
            score: 0,
            logo: "",
          },
        },
      ],
    });

    return {
      matchupsList,
    };
  },
};
</script>

<style scoped>
.container {
  display: flex;
  flex-wrap: wrap;
}

.matchup-schedule {
  flex: 1 1 50%;
  max-width: calc(50% - 32px);
  box-sizing: border-box;
}

.football-news {
  flex: 1 1 50%;
  box-sizing: border-box;
}

@media only screen and (max-width: 768px) {
  .container {
    flex-direction: column;
  }

  .matchup-schedule,
  .football-news {
    flex: 1 1 100%;
    max-width: 100%;
  }
}
</style>
