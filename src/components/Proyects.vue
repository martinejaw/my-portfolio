<template>
  <!-- Portfolio Section-->
  <section class="page-section portfolio" id="portfolio">
    <div class="container">
      <!-- Portfolio Section Heading-->
      <h2
        class="page-section-heading text-center text-uppercase text-secondary mb-0"
      >
        Portfolio
      </h2>
      <!-- Icon Divider-->
      <div class="divider-custom">
        <div class="divider-custom-line"></div>
        <div class="divider-custom-icon"><i class="fas fa-star"></i></div>
        <div class="divider-custom-line"></div>
      </div>
      <!-- Portfolio Grid Items-->
      <div class="row justify-content-center">
        <PortfolioItem
          v-for="proyect in proyects"
          :key="proyect.nro"
          :imgSrc="proyect.imgSrc"
          :header="proyect.title"
          :body="proyect.description"
          :tags="proyect.tags"
        />
      </div>
    </div>
  </section>
</template>

<script>
import PortfolioItem from "./PortfolioItem";
export default {
  components: { PortfolioItem },
  data() {
    return {
      proyects: [
        {
          nro: 1,
          title: "Parser Pseudocodigo",
          description: "Este es un parser hecho con FlexBison",
          imgSrc: "img/portfolio/cabin.png",
          tags: ["Flex", "Bison"],
        },
        {
          nro: 2,
          title: "Centros Hospitalarios COVID",
          description: "WebApp con Express, Vue y MySQL",
          imgSrc: "img/portfolio/cake.png",
          tags: ["Vue", "Express", "MySQL"],
        },
        {
          nro: 3,
          title: "Simulador CPU/Memoria",
          description: "Este es un parser hecho con FlexBison",
          imgSrc: "img/portfolio/game.png",
          tags: ["Java"],
        },
        {
          nro: 4,
          title: "Mapa Interactivo",
          description: "Este es un parser hecho con FlexBison",
          imgSrc: "img/portfolio/submarine.png",
          tags: ["React", "OpenLayers", "PostGIS"],
        },
      ],
    };
  },
};
</script>

<style>
</style>