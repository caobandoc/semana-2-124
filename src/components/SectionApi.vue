<template>
  <div>
    <div class="row row-cols-2">
      <div
        class="border border-light pdgd"
        v-for="(news, index) of news"
        :key="index"
      >
        <div class="float-left">
          <img
            :src="news.urlToImage"
            alt=""
            class="rounded float-left img-thumbnail"
            width="400"
          />
          <p>Noticia completa: <a :href="news.url">Aqui</a></p>
        </div>
        <div class="pdg">
          <h3>{{ news.title }}</h3>
          <p>
            {{ news.description }}
          </p>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import axios from "axios";

export default {
  name: "SectionApi",
  data() {
    return {
      news: null,
    };
  },
  mounted() {
    axios
      .get(
        "http://newsapi.org/v2/top-headlines?country=co&apiKey=707434e98d124a42ad382e9fe1ec1cf4"
      )
      .then((response) => {
        this.news = response.data.articles.slice(0, 4);
      });
  },
};
</script>

<style scoped>
.img-thumbnail {
  margin-right: 10px;
}
.pdgd {
  padding: 15px;
}
</style>