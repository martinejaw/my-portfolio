<template>
  <!-- Imagen -->
  <div class="col-md-6 col-lg-4 mb-5" @click="showModal = true">
    <div class="portfolio-item mx-auto">
      <div
        class="portfolio-item-caption d-flex align-items-center justify-content-center h-100 w-100"
      >
        <div class="portfolio-item-caption-content text-center text-white">
          <i class="fas fa-plus fa-3x"></i>
        </div>
      </div>
      <img class="img-fluid" :src="imgSrc" alt="" />
      <div class="info">
        <h4>{{ header }}</h4>
        <div class="tags">
          <p
            class="tag"
            v-for="(tag, index) in tags"
            :key="index"
          >{{ tag }}</p>
        </div>
      </div>
    </div>
  </div>
  <Modal v-if="showModal" @close="showModal = false">
    <template v-slot:header>
      <h1>{{ header }}</h1>
    </template>
    <template v-slot:body>
      <p>{{ body }}</p>
    </template>
  </Modal>
</template>

<script>
import Modal from "./Modal";
export default {
  props: ["imgSrc", "header", "body", "tags"],
  components: {
    Modal,
  },
  data() {
    return {
      showModal: false,
    };
  },
};
</script>

<style scoped>
.tags {
  display: flex;
}
.tag {
  border-radius: 20px;
  background: greenyellow;
  padding: 4px 14px;
  margin: 2px;
  justify-content: flex-start;
}
.portfolio-item {
  border: 1px solid grey;
  border-radius: 10px;
}
h4 {
  font-size: 15px;
}
.info {
  margin: 10px 20px;
}
</style>