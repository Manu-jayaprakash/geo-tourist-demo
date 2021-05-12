<template>
  <el-tabs v-model="activeName" class="content-tabs">
    <el-tab-pane
      v-for="item in tourData"
      :key="item.id"
      :label="item.language"
      :name="item.language"
    >
      <div class="tab-content-wrapper">
        <div class="place-details">
          <div class="place-details-image">
            <img src="../../assets/pic.png" alt="place" class="place-image" />
            <span class="set-cover-btn">
              <font-awesome-icon icon="camera-retro" />Set cover</span
            >
          </div>
          <h1 class="place-details-heading">{{ item.heading }}</h1>
          <p class="place-details-description">{{ item.content }}</p>
        </div>
      </div>
    </el-tab-pane>
    <el-button round icon="el-icon-plus" class="add-btn">Add...</el-button>
  </el-tabs>
</template>

<script>
export default {
  name: "ContentTab",
  data() {
    return {
      activeName: "English",
      tourData: [
        {
          language: "English",
          id: 1,
          heading: "A WALKING TRAIL OF MONTMARTRE, PARIS",
          content:
            "Dominated by the grandeur of the ever-visible Sacré-Cœur Basilica, the leafy hilltop village of Montmartre was once the play area of Paris’s most famous artists, bohemians and creatures of the night. These days, the winding cobbled streets host chic cafes, retro boutiques and fine French dining but, if you look closely enough, those in search of historical secrets can still find traces of the old La Bohème hidden between the tourist traps…",
        },
        {
          language: "French",
          id: 2,
          heading: "UN SENTIER DE MARCHE DE MONTMARTRE, PARIS",
          content:
            "Dominé par la grandeur de la basilique du Sacré-Cœur toujours visible, le village verdoyant de Montmartre était autrefois l'aire de jeux des artistes, bohèmes et créatures de la nuit les plus célèbres de Paris. De nos jours, les rues pavées sinueuses abritent cafés chics, boutiques rétro et gastronomie française mais, si l'on y regarde de près, ceux en quête de secrets historiques peuvent encore trouver des traces de l'ancienne La Bohème cachées entre les pièges à touristes…",
        },
        {
          language: "Deutch",
          id: 3,
          heading: "EEN WANDELPAD VAN MONTMARTRE, PARIJS",
          content:
            "Het lommerrijke heuveldorp Montmartre, gedomineerd door de grootsheid van de altijd zichtbare Sacré-Cœur-basiliek, was ooit het speelterrein van de beroemdste kunstenaars, bohemiens en nachtwezens van Parijs. Tegenwoordig zijn er in de kronkelende geplaveide straatjes chique cafés, retro-boetieks en fijne Franse restaurants, maar als je goed kijkt, kunnen degenen die op zoek zijn naar historische geheimen nog steeds sporen vinden van het oude La Bohème verborgen tussen de toeristische lokazen ...",
        },
        {
          language: "Spanish",
          id: 4,
          heading: "UN SENDERO A PIE DE MONTMARTRE, PARIS",
          content:
            "Dominado por la grandeza de la siempre visible Basílica del Sacré-Cœur, el frondoso pueblo de Montmartre en la cima de una colina fue una vez el área de juegos de los artistas, bohemios y criaturas de la noche más famosos de París. En estos días, las sinuosas calles adoquinadas albergan elegantes cafés, boutiques retro y excelentes restaurantes franceses, pero, si miras con atención, aquellos en busca de secretos históricos aún pueden encontrar rastros de la antigua La Bohème escondidos entre las trampas para turistas ...",
        },
      ],
    };
  },
};
</script>
<style>
@import "./ContentTab.css";
</style>