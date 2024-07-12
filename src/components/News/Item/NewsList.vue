<template>
  <div class="news-list">
    <div class="news-list-title">
      <h3>NHẬN ĐỊNH BÓNG ĐÁ</h3>
      <a href="#">Xem tất cả</a>
    </div>
    <div class="grid-container">
      <div v-for="(news, index) in newsList" :key="index" class="news-item">
        <img src="../../../assets/anh_mo_ta.png" alt="News Image" />
        <div class="news-content">
          <span>{{ news.title }}</span>
          <p>{{ news.date }}</p>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import { ref } from "vue";

export default {
  setup() {
    const newsList = ref([
      {
        title: "lorem ipsum dolor sit amet, consectetur adipiscing elit.",
        date: "2021-09-01",
      },
      {
        title: "lorem ipsum dolor sit amet, consectetur adipiscing elit.",
        date: "2021-09-01",
      },
      {
        title: "lorem ipsum dolor sit amet, consectetur adipiscing elit.",
        date: "2021-09-01",
      },
      {
        title: "News 2",
        date: "2021-09-05",
      },
      {
        title: "News 2",
        date: "2021-09-05",
      },
      {
        title: "News 2",
        date: "2021-09-05",
      },
      {
        title: "News 2",
        date: "2021-09-05",
      },
      {
        title: "News 2",
        date: "2021-09-05",
      },
      {
        title: "News 2",
        date: "2021-09-05",
      },
      {
        title: "News 2",
        date: "2021-09-05",
      },
      {
        title: "News 2",
        date: "2021-09-05",
      },
      {
        title: "News 2",
        date: "2021-09-05",
      },
      {
        title: "News 2",
        date: "2021-09-05",
      },
      {
        title: "News 2",
        date: "2021-09-05",
      },
      {
        title: "News 2",
        date: "2021-09-05",
      },
      {
        title: "News 2",
        date: "2021-09-05",
      },
      {
        title: "News 2",
        date: "2021-09-05",
      },
      {
        title: "News 2",
        date: "2021-09-05",
      },
      {
        title: "News 2",
        date: "2021-09-05",
      },
      {
        title: "News 2",
        date: "2021-09-05",
      },
      {
        title: "News 2",
        date: "2021-09-05",
      },
    ]);

    return {
      newsList,
    };
  },
};
</script>

<style lang="scss" scoped>
.news-list {
  &-title {
    display: flex;
    justify-content: space-between;
    align-items: center;
    margin-bottom: 20px;
    color: #ff004c;
    border-top: 4px solid #ff004c;
    padding: 12px 12px 0 12px;

    h3 {
      margin: 0;
    }

    a {
      color: black;
      font-weight: bold;
      text-decoration: none;

      &:hover {
        text-decoration: underline;
      }
    }
  }

  .grid-container {
    display: grid;
    grid-template-columns: 1fr;
    grid-gap: 20px;
    min-width: 300px !important;

    @media only screen and (min-width: 768px) {
      grid-template-columns: repeat(1, 1fr);
    }

    @media only screen and (min-width: 1024px) {
      grid-template-columns: repeat(2, 1fr);
    }

    .news-item {
      display: grid;
      grid-template-columns: 50% 50%;

      img {
        width: 100%;
        height: 100%;
        object-fit: cover;
        border-radius: 8px;
      }

      .news-content {
        display: flex;
        flex-direction: column;
        justify-content: space-between;
        align-items: flex-start;
        margin-left: 10px;
        text-align: left;

        span {
          margin-top: 0;
          font-weight: 600;
        }

        p {
          margin-bottom: 0;
          font-size: 12px;
          color: gray;
        }
      }
    }
  }
}
</style>
